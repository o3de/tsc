# TSC Meeting - 7/09/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Adam Dabrowski
* colinb[APMG]
* Gl3D
* Jan Hanca [Robotec.Ai]
* Joe Bryant [O3DF]
* Lloyd T. [Carbonated]
* Luis Sempé
* Mike S. [Carbonated]
* Naomi Washington [LF]
* Nick_L
* Steve P. [Amazon]
* Tobias Alexander Franke [Huawei]

## Agenda items

### Agenda Item (Official) - o3de-extras discussion
* Huawei was trying to get a change in
* They could not pass AR, they put their own branch O3DE-Extras (700 changed files) to pass AR
* They reverted their changes in O3DE-extras afterwards.
* Thats an awfully big workaround, and its a dangerous workaround to get something thru AR.
* Mike wanted to raise that red flag. 
  * Red flag 1 - someone should have talked to stakeholders about the issue and allowed to figure out a solution without replacing all of o3de-extras
  * Red flag 2 - our AR is becoming more of a hinderance than a help.  We want to take all the failing tests out and yank them from now.
* For o3de-extras its a very large problem.  Once every couple of days this is not passing AR and has nothing to do with the code.  AR is flaky for o3de-extras.

(Technical discussion ensued)

* Tobias will go into Huawei chat and discuss it.
* Joe:  Lots of concerns about o3de-extras and pinning it to releases and the release process.  you have mentioned you are not really keen on.  O3de-extras is becoming as complicated as o3de-development.  We need to sit down and figure out what a sane plan for o3de extras actually is.
* Keep O3DE extras working and get thru AR.
* Joe:  Discussion with Robotec.AI and other stakeholders is required.  What is the process for maintainers.
* Joe:  Please include Mike Chang in the discussions about any pipeline issues / AR Issues.
* Joe:  This is a gap in our docs for when we create branches.  We have to make sure all the repos.
* Colinb: all of these things are written in the TLDR/original document.  They must remain in sync for the releases, was probably a missing piece.  Order of operations.
* Steve P: One more issue, even if we update stabilization for o3de-extras, it doesn't mean that those updates are retrieved.  Another gap in the checklist is the version list.
* Joe:  Why do we have stabilization on a different internal release versioning than development?  Originally it was because the releases march at a slower rate for development and testing.   Maybe as a part of the discussion, I think we need to revisit how we do the versioning, maybe at least the internal version has to track with dev somehow, so we aren't running into all sorts of issues.
* Joe:  Internal version is more about feature set compatibility, engineers can use the internal version to know whats compatible with what versions.
* Joe:  Conversation: Does our versioning plan work?
* colinb: Some of the changes I'm contemplating for Schema 2.0 does have some relevance there, because of how versions are actually written into the object files themselves.
* Joe:  Scope of change would be large.  So it would need RFC.

* Joe: We'll have a meeting - 3 things:  
  * O3DE-extras - new stabilization branches
  * Joe:  2. holes in our plan
  * Joe:  3. our versioning system

### Agenda Item Ad-hoc - Joe - Michael P. - Engine Overview
* Joe: Michael P has been putting together an amazing document for everything and antyhing that exists in o3de.  All of the different 3p things that include, all the features, modules, editor, etc, when I looked at it I thought it was awesome for contributors to get a lay of the land.
* Joe:  I talked with them, can we put it up somewhere, maybe on github, doc piece, etc, and for Joe to use to talk to new companies about o3de, its great to have all-in-one-document.  All the technical pieces of o3de.  I was curious, Nick, could you take a look at it?
* Works for a really large company, working on O3DE, they requested a document like this, to approve working on an Open Source project.  That's the reason its closed.  There's nothing actually private or secret in this document.
* Nick: Could be a good doc for a wiki (living document)
* Joe: This would also help carbonated.
* Lloyd: Onboarding engine remote is a pain.  I'd happily consume the doc.

(Discussion about github wiki) - Its a proper wiki, has anyone can edit, can update often, can revert.

### Agenda Item Ad-hoc - Joe - Leave if you want to!
* colinb - chairs, when you do your triage, for PRs, please tag them to SIGs.
* If you have a label on your PR, have it always come up.
* We could label with needs-sig automatically
* We could tag with sigs automatically based on codeowners.
* Colinb: is currently doing that for everybody.
* Joe:  LEt's talk about them in terms for making it easy for contributors to adhere to what we need.  We survive on our contributors.  Thankful for what they're doing.
* Joe: Getting reviewers, at least you can try to get people to review, by nagging.

### Agenda Item Ad-hoc - colinb - to move the objects into extras from o3de
* colinb: work was stopped on this object was duplicated and the work was stopped when they left their company.  Anyone taking up the mantle?
* Joe: Nobody is volunteered or assigned.
* Joe:  Only requirement is that before we do anything final/do anything final, there has to be TSC buy-in.  we don't want to surprise users.  Installation has to be as easy as possible.
* Steve: Audio/WWISe was moved.  It might be misleading since hte folder is still there, but there's a readme that says its been moved.  Migration is complete.
* Joe: Colin, work with people/sigs, co-chairs, etc figure out how we want to solve it moving forward, get it documented, etc. 

### Agenda Item: Lloyd - Thread timing
* Lloyd: granular thread timing system is coming, helping us finding cpu starvation.
* Lloyd: Need someone to help bring it over, we are swamped
* Lloyd: Audio gem was starving the CPU on device/mobile/ios

* Who was the knowledge about the characters with the most knowledge about skins/lods.
* Talk to Galib
