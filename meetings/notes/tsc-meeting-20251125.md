# TSC Meeting - 11/25/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L. A.
* Astin A.
* colinb[APMG]
* Gaian Helmers [Genome Studios]
* Hellaenergy (Nick) [Red Hat]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* JTc[SCB_GameDesign]
* Matteo [Loherangrin]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]

## Meeting Notes

### Announcements - Hellaenergy (Nick)
* Sig-release is trying to be on track on the point release for 2 weeks from today.

### Discussion - mimalloc discussion
* We are not arriving at a mimalloc discussion yet, we need to iron out all the loose ends, specifically, we might want to disable
  the HPHA allocator by default, and use mimalloc to fill in any perf gaps.
* We need to answer some benchmark questions properly first, and figure out if there are any linux or other platform issues.
   * Crashes  in tests
   * Benchmark in real tests like opening a big level, compiling assets, etc., compare the 3 configs.
* JT [SCB_GameDesign] - Embedded robotics usecases, need that smaller footprint.  Its something that researchers will look into
  in embedded systems and specially since ROSCon comes out embedded in a soc platform.  We do have to make sure we can accomidate.

### Discussion - Entity Activation System - Gaian Helmers [Geonome Studios]
* Adds: Start Inactive, Parent / Child heirarchy activation, where if you deactivate a parent, or root of prefab, all the children
  fall inactive in lockstep
* Definitely a deeply entrenched system, messing with Entity, confident in what we've put together, completeion wise its 98%, it
  needs validation, descriptions can be improved, cosmetic things.
* I wanted to summarize whats been changed and whats been happening.
* Thanks to Nick for exposing the button for "start inactive".
* We used to have a boolean for "active / inactive" and an enum for current state
* Now, we introduced a bitmask (32 bit integer) which lets us flag up to 32 flags for active or inactive.  And so the logic in it
  is if all the factors / flags are active, the entity is an active, and works as before.
* We have the parent active type, now.  By segmenting these active types into their own flag we can do non destructive changes of
  state, you can have a parent become inactive and the children become inactive but don't lose their state.
* I went into the transform component and shifted some things around.  First and formost, when transform was deactivated it would
  do this really destructive thing where it would dump all of its parent data and stuff, and then alter its translation.  Thats
  why when you deactivate and reactivate a thing the positioning of all the child entities would explode.  This would devestate
  the composition of entities in the heirarchy.
* What I've changed is I've moved from activate/deactivate to init/destructor, in order to make it so that transform component
  (which is treated specially) when the transform comes into existence it stops on destruction.  This allows you to request its
  parent, children, reparent, etc, otherwise access its transform functionality regardless of whether its in an active state or
  not.  Already-present logical flows just like when a parent goes inactive, instead, it no longer destroys all its data and
  uses that same event to set their own parent inactive flags.
* The same format of recursion, reparenting, translations passing down the chain, the recursion that drives the child activate.
  It all works really well.
* The transform component is a lot more stable and usefil with this, the functionality is made accessible.
* In benchmarking the comparison from this transform driven heirarchy stuff and flag driven activation is indistinguishable
  from original dev branch normal functionality.  While it could use brilliant polish to the Nth degree, this is fully functional.
* Notes:  Benchmarking numbers were nearly indistinguishable, every component was compatible except for one landscape compnoent,
  I didn't test landscape component, and I could not test multiplayer components.  I summarize int he doc in my post here, its
  a very non destructive process, its playing with the existing systems already at play.  I think the only way multiplayer
  could be incompat is synching the call to active/inactive.
* What still needs to be done:  This whole piece was established so we can shift over to creating async spawning, with activation
  stuff already established.  I've tested everything, fixed the last few mistakes, review editor only flag and how it behaves
  and its working before any other activation events.  But when it comes to deployment I don't think anyones.
* 10k entities speed was negligible from baseline.
* You can strategically activate by spawning, by using start active by start.  So my benefits, I can load levels over time,
  loading the core pieces, then core pieces and activating incrementally, lazy loading.  Great benefit to the delta time between
  two frames.  The delta time between load and play frame was 7s delta, so huge gain there.
* Matteo [Loheragrin] - are we planning opt in or opt out compatibility?
* this needs to be a ImpactFul change.  Reaches into scene graph / depth graph USD stuff.


