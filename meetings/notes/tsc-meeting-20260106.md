# TSC Meeting - 1/06/2026

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L. A. [O3DF]
* colinb[APMG]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Mike_C [Amazon]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Joe Bryant
* We should look into doing in a .2 release to address the issues with visual studio (latest version) unless there's something
  else I'm not aware of.  We should just do that for the .2 release and nothing else.
* Nick L: I have a fix for this, ready to go.
* Community edition forces you onto the latest, 2026, its difficult to get the old one.

### Announcement - Joe Bryant
* I'm out 8th to 18th (jan), I'll not be reachable, but I'll check in periodically.  I won't have access to anything at that time.
* I'll be in on 19th.

### Announcement - O3DE Connect
* Wednesday Jan 21st 2026 will be year in review.
* Joe:  Mike and I will be talking about our 2025 downloads and other numbers.  Dramatic increase for 2025.

### Discussion - AR for release
* AR will continue on the oldest version of VS on it.
* It needs to be tested somehow.

### Discussion - Mac working
* The mac version is a focus this year. (Joe)
* We can release it as preview mode, but then get help improving it.  We are talking about the client/tools.
* Mike C: Does LF have an apple account we can use?  we would need one with signing keys.
* Joe: A  working groupw would make sense for this, and colin_b would be the person to talk to as the chair for sig-platform. 
  We should set up a working group for mac so we can have a concentrated effort on it.
* Lots of interested parties in mac.
* We are part of ASWF and they use linux and mac not windows.
* Linux and windows are pretty equal from priority perspective.
* 2026 Priority is mac "Get it up and running" on ARM MAC
* There will be a maintennence cost we have to pay, when we launch the mac version we have in place a plan to supporting/maintaining it.
* Nick: Mac AR has to come online, somehow.  We can't require users to get or buy a mac to test their PRs.
* JT: We need to bring the mac up to speed, and we need mac artists.  This engine is pretty sterile looking and we need to push for artwork.
* This is critcial for way more than mac support, we also need the creative talent.

### Discussion - Beautiful corner
* colinb: we do need a starterproject or something that sizzles, something that gets people to look at it.
* Joe: AKA beautiful corner.
* JT: I have the multiplayer sample project, to get it as part of a user content jam.  We need artists to create stuff.
* JT: I'm working hard at making the MPS one of the samples in showcase pieces.  I've made tremendous strides.

### Mike_C - Going to be making an announcement to switching off jenkins to GHA
* EArly next week or this week.
* Retry mechanism is coming into place, it won't block folks
* We put a notice, if we run it on your own branch or fork, running windows is going to take a long time.
* Its going to have to be something you retry if you take too long.
* You can retry at the last point it started it, you can deploy it in your own fork.
* The idea is that we turn off Jenkins AR to be the blocking portion of the PR and be enabling it in GHA going forward, prior
  to the next release.  How difficult is it to go back and forth.
* Its a button click to turn on and off the reqs, but we'll give it a bit of time to bake forever, we want to see a good number
  of things succceed, and want to make sure people are comfortable with this arrangement.  We want to start offlining the infra
  and if we really need to bring it back up its still possible to bring it back up.
* colinb: Github charging for GHA runners?
* Mike_C:  It was for BYO build, they'd charge you for the same amount as a standard build for the connection fee. 
* They rolled that back after a bunch of people kicked up dust about it.
* We are using their instances and public repos they are not going to charge us for that.
* JT:  The pushback last time was a lot of big names in the OS community.  hopefully the good graces would continue.

