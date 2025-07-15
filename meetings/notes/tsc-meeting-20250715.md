# TSC Meeting - 7/15/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L.A.
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* Jack420 WARDADDY
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Luis
* Matteo [Loharangrin]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amazon]
* Steve P. [Amazon]

## Meeting Notes 

### Announcement - Joe Bryant
* Will be doing an AMA for September's O3DE-Connect meeting (90 minute long)
* August 13th will be the upcoming O3DE connect.
* September 10th will be the AMA.
* I will be out for most of August, then going on PTO.  I'll be out
  from the 9th until the 26th of August.

### Announcment - We are planning for the point release .1
* Soon we will create the official task
* Can you ask mike to ask the release candidate so people can start testing
* We will postpone any remaining concerns for next point or next release.
* July 22 is the release.

### Announcement - JT
* Local UX group attended, did a UX experience slam.  They also have a popoular
  slam out called a Game Slam, so I'm working on a Game Slam for O3DE.
* Slams are very popular events today.  There are already game slam templates.

### Discussion - Agenda Item - meshoptimizer - Nick L
https://github.com/o3de/o3de/pull/18711
https://github.com/zeux/meshoptimizer
* We will have to meet the license requirements for MIT, including disclosure.
  See license scanner!
* TSC generally approves of this.

### Discussion - Doc/Sig/Community
* JOE:  We discussed reorganizing discord - removing channels, adding channels,
  in order to make it easier for newcomers to know where to go, and how to ask
  questions, etc.  Also to make it eaiser for sigs not to have to check 15 different
  sig-chats to answer questions, etc.  
* We will be removing one of the support channel, so theres just 1 support channel
  to look at.  Gaian did create a test-server with the changes on there, and I'll
  ask Gaian to go post it publically, and ask people to go on there, check it out,
  see what they think. 
* We have a design, and a test server, so these changes are coming, probably some
  time in the summer.
* Colinb: Build status channel - always broken, all the time.  We are going to
  talk to Mike Chang.  If we can't get it fixed, we may just remove it.  It has
  not been used since 2022.  
* Joe:  We will try to revive it, and if we can't, we'll remove it.

### Discussion - Steve P [Amazon]
* Joe:  My thoughts - I would like to get it into the next release, however,
  that is an opinion from the ED.  Ultimately, HellaEnergy (nick), and Matteo
  will have the decision.
* Cut two different branches - one before, one after the merge.  
* Joe - Easiset way for Mike, Matteo, and Nick to handle this, is to wait to cut, and then cherry pick everything all around that.  How much risk they're willing to take for this release.
* Joe:  While we do want to create a release before ROSCON, just because it helps
  compound the marketing and such, if its not ready, its not ready, and we hold it.
  They will forgive if late, they will not forgive if they release an extremely
  buggy build.  
* Joe:  Ultimately its up to matteo and hellaenergy.
* Steve P.  I would still like to get someone from sig-graphics and sig-platform
  to review it.  Those are the key areas.  There was (outside of AZCore), atomcore
  was already a shared dll, I had to refactor it, but they seem to be fine so.
* Steve p.  The way things are exported are slightly different from clang to cpp,
  that could be reviewed.
* Steve P.  Besides decalring the exports, its for compile time changes.
* Steve P.  The one issue I was concerned about the most, we had o3dekernel, which
  we dont' need one anymore.  There was an issue about how things were exported
  and shared.
* Steve P.  That was the risk area.
* Matteo:  Just to understand:  do you have a plan for extending the same approach
  to other gems.  Do we try to move atom, other gems to the same shared approach?
  This may be a need to evaluate if we want to release all the new approach
  altogether or break it up into separate releases.
* Steve. P. : AtomCore was a library with symbols.  In terms of other libraries
  converted to shared, AzNetwork.  Anything thats a library (not a gem), that would
  be possible to convert.
* JT: Question for Jan, will any groups be delving into the engine itself, or will
  they be hanging out in gems
* Jan:  I did compile and test it with simulation I'm working on with a client, 
  and did not see anything weird happening, I don't think it would hurt simulation.
* Joe:  Do we think robotics engineers ar going to be in simulation code or will
  they get into engine code?   I think they may migrate to engine code.
* JT:  Real world timing in the robotics system, perhaps.  Did Jan see any
  extension of robotics for developers to get into the core APIs.  
* STEVE Anyone debugging linux will love this fix, loading modules through 
  lldb, and every  module loads much quicker.  Having those debug symbols in
  the modules, they were gigantic.  We saved a ton of size for there.  Its
  workable for debug w/o workarounds.  Prior we had to delete debug files,
* Joe: this is hugely beneficial for people, especially one of our target
  audiences, making robotics in linux.  If we have to postpone the release,
  we can, but its up to Release to determine this.
