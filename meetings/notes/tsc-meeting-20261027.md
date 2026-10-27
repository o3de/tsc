# TSC Meeting - 10/27/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Andre L.A.
* Astin[Chogan]
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* hex
* Iris [Coffee-Road Studios]
* Jan Hanca [Robotec.ai]
* JT[SCB_Network]
* Mike_C [Amazon]
* Nick_L
* Noone (Chogan)
* Re'Baal
* RoddieKieley [Red Hat]
* Sergio Rojas
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* std::vector<_> P-Rose
* Steve P [Amazon]
* Ulrick28

### Announcement - Nick (Sig-Release) 
* Release is planned tomorrow - we might have an issue which we may have to address.
* Issue was fixed and rebuilt into the stabilization test binaries.
* I found another - PR 20241 - https://github.com/o3de/o3de/issues/20241
* Segfault in tests.  Run in manually.  Running it automated.  Running it manually to see if it exists
  without scripting.
* I might be reporting another issue on top of that.
* Nick:  Does anyone depend on this being released right now?
* (Group response): We are not aware of anyone waiting, and if they are desperate they can get Stabilization.
* (TSC): Group votes to delay - go for quality.
* Ulrick28: Delay the release, the latest we recommend is november 15th.
* Once you get to USA Thanksgiving, December is basically done, they take longer breaks.
* Consider November 11th.
* DCO Issue?
* Mike_C - If it becomes an onerous issue we could reopen that investigation.
* Ulrick28 - we can open convo with naomi, ask, Who do we talk to about this?
* Ulrick28 - Beyond maintaining it I don't know what they do to it.
* Mike_C to check for other solutions / better solutions / proposed resolutions.

### Discussion - (Agenda) - Agenda Item:  Discuss Priveleges for Github
* Ulrick28 - We need to cull the list of maintainers / Admins.  
* Sig leaders need to determine if permissions are stale.
* Adding new reviewers or maintainers, to the list, and the way the system works is that each sig has their own list of maintainers 
  and reviewrs, and those bubble up to the master list of maintainers and reviewers, and that bubbles up permissisions to who can merge.
* For `main` there are only 3 people that can submit (possibly up to 4).  But I need Nick_L approval
* Nick_L: You have my approval
* Hellaenergy (Nick) [Red Hat] - Will we create an issue to track this?
* Ulrick: peopel generally ignore it but I'll create one.
* JT[SCB_Network] - we have gotten further from bylaws and procedures, we need to get back to if we can, if its practical to have more formality
  with what we do, tracking things, keeping things out in the open, so a lot of things are not done behind the scenes, have transparency.  Revise
  that project so its a strong structure for new people and continue our onboarding and scaling.
* Mike_C [Amazon] - Teams also exist for sigs, and Team Owners.  Definitely let us know if someone needs to be a delegate for something like this.
  Thats the person that lets you in.
* Ulrick28:  The chairs and co chairs need to have permissions to update their teams, for their SIG, thats part of the job of chair.
* Some SIGs are pretty inactive so we need to make sure that cleanup is still happening.
* Ulrick28: I used to do it every 6 months.
* colinb: Can we get a checklist or runbook or list of expectations for sig leaders?
* Ulrick28: Would be a good idea to have that checklist or runbook, yes.
* JT: I'll take that notion, and there's definitely different ones in each sig, different information where we had RIF, little bit of cleanup will
  really make the sigs look a lot more presentable to people.  UI/UX for example really stands out.

### Discussion - (Carry Over) - Astin [Chogan] - Atom to be more user friendly
* Astin: I ahve been working with Gaian and analyzing atom for the last 2 months.
* We made a document about how to improve it in many decent ways.  Its a deep technical document, would not be good to share here.
* I can start a talk in one of the sigs after that and present it there.  Plus some optimization / tiny changes that can help optimization
  since it was brought up last week and added to the document.
* Main goal of bringing it up in the meeting today is opening up the conversaition about improving atom as it is one of our harder bottlenecks
  and hard to work with artists who are not technical.  Its been a big issue when I've been bringing people from the industry to O3DE, and they
  have an issue about how Atom handles stuff.
* Ulrick28: Are you talking about the rendering system, or the tools?
* Astin: Like creating shaders, passes and shaders, there are issues with issues like passes is not being compiled or not going to render it, there
  are a lot of minor issue that makes the user experience hard to deal with.
* Astin:  Optimization and making it look better can be done outside there, obviously.
* Colinb: Is this for TSC because its a structural issue?
* Astin: More of a structural issue to get consensus from the community and the leaders
* Sid_Moudgil [Amzn]: You are hitting the nail on some of the parts of Atom we did not emphasise a lot of work on. 
* Sid: Most of the innovation and research went into the features for the rendering engine itself polished and extensive.
* In terms of tooling we didn't expect artists to be adding shaders, new pipelines, passes.  So it got de-prioritized
* We had folks did a lot of videos and the videos were fairly complicated, we had a very complicated set of videos, hundreds of steps you have
  to go through it.  It is one of those areas that is lacking.  If you have improvements, please consider them inside the editor and how they
  can be extended in the editor, and how the editor could be extended and making it so that inside the editor its like "Hey there's the pipeline
  I'm running and..." and there were plans for a full GUI tooling for passes and see the full pass tree in a gui, and then play around with it
  all of those are nice to haves, those are usually very few folks will use it. 
* Making it extensible so you can build more pipelines, passes.  You know the engine enough to add pipelines, passes, so I think that we 
  deliberately deprioritized this since we felt very few folks would be deep in the guts of the engine and making these changes.  We figured
  that most artists would just enable/disable features.  But now you are actually doing more architecturally different.  I can take a look
  at the doc, paste it, tag me in.
* Astin(Chogan) I will prepare a talk in the sig channel?
* (It is better to do asynchronous types of documentation - docs, videos, etc) people are in all sorts of time zones.  Anything someone can
  get up and watch at any time is best to communicate.  Wiki, too.
* Colinb: or start a workgroup
* Ulrick28:  How is our process for creating workgroups?  I gotta get Naomi on this, can we just make them?  I'd like to create a WG for AI
  but we're stalled until I've found a process for it.
* JT: There needs to be a write up on WG and there needs to be a paper trail, resources are assigned like repos, etc.

### Discussion - (Agenda) - JT - ECS vs ECS topic
* JT: CES vs ECS https://github.com/o3de/o3de.org/discussions/2803
* I suggest we defer that for next release.  Its causing confusion for people!
* Over the course of the next release we are looking at reorging the docs extensively.

* JT: Hellaenergy, do you need help with the move of the release?
* 11th is veterans day.
* We can cover that in sig-release.  Getting out the comms.

### Next week topics
* Iris:  Main problem is that the studio audio guy who composed all the music and so does not have a proper middleware
  that is also in a sense that is usuable.  Miniaudio isn't usable.  WWise is not up to date anymore, so there is not an easy to use
  way of doing things for audio people to do audio in the engine.  Fine for smaller projects, bottleneck for bigger projects.
* Mike_C - Archiving discord topics for searchability.

