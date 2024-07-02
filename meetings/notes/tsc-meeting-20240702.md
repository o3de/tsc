# TSC Meeting - 7/02/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Joe Bryant [O3DF]
* Lloyd T. [Carbonated]
* Luis Sempé
* Mike S. [Carbonated]
* Naomi Washington [LF]
* nick_l
* null [meta]
* RoddieKieley [Red Hat]
* Steve P [Amazon]

## Agenda items
https://github.com/o3de/tsc/issues/131

### Agenda Item (Official) - Joe - Release Schedule
* Release Schedule Proposal put together
* Monday Aug 5th, 2024 - Feature Lock
* Monday Sept 2nd -Art and splash lock
* Tuesday sept 25th, 2024 - Full Code Lock
* Prerelease Dry Run  - Monday Oct 7th 2024
* Release - Wednesday Oct 9th 2024

Goal is to release before ROSCON 2024 (Oct 21st - 23rd, 2024)

Community focused stabilization testing - 2 or 3 days scattered throughout the stabilization process.  Tell people to grab the build, test it, report issues, etc.  We need to come up with dates and a plan for that.

* Colin:  Will this release not include a snap package? 
* Joe: we'll talk about that with sig platform
* Joe:  we talk with Canonical as well.  Leaning towards removing it, but have to consider all the community impacts.  I absolutely want to support Fedora.  Red Hat is a member of hte o3de foundation.
* Nick:  is it code incompatibilities or packaging?
* RoddieKieley: Its mostly a packaging thing.  One is "could we package it and make it work?"  And then there's the "could we get it into the official fedora package system?" Thats a much higher bar and has extra rules.  We're not too far off.  The next part off it "what are we building and testing from the foundations point of view to make sure it stays okay once we've done the work to keep it going?"
* Joe: I think building packages for fedora is going to be a lot simpler than the snap packaging.
* RoddieKieley:  "Containerization is also always a challenge for graphical stuff"
* Joe: First step is getting it accessible, uploaded, so people can download it and it works.
* It can be on COPR without being blessed and pure.
* RoddieKeiley: COPR is not so much a store as a package distribution system itself.
* Steve P: we have our internal python
* Steve P: RFC exists for snap removal.  Aside from download binaries, there's debian lists you can host yourself.
* Which SIG would tackle a QT update?

### Agenda Item (Official) - Naomi - Discord cleanup status
* Let everyone know on discord, RFC on GitHub, as you all know our discord is full of unused channels.  We want to start deleting or archiving some of these channels or merging some.  We wanted to also look at the roles.  A lot of people are maybe not working ont he project.  We wanted to do a general cleanup.  The Call for comments was open for a little over 2 weeks.  we didn't get anything, going to move forward with what I proposed.

### Agenda Item (Official) - Naomi - Github Maintainer Cleanup
* The LF is going to roll out a survey to project maintainers.  Our maintainer list in github is not cleaned up at all.  I talked to Joe,a nd Iw ill be sending out an email to the SIG-Chairs to go thru and look at who their maintainers are for their individual sigs.  I'll send it out in an email and etc.  then I will send it to (Nick and Joe) to get the final say.  I'll clean it up in GitHub
( https://github.com/orgs/o3de/teams )

* We will have a set mailing list moving forward.  But after cleanup we need to establish an official one.
* Joe:  One thing about maintainership, your maintainership/reviewer privs are based on activity.  You get them by having x number of reviews/etc.  You lose them by being inactive for 6 mo, you lose your privs.  You can always reapply for activity.
* https://github.com/orgs/o3de/teams/maintainers/teams
* So we need to audit and remove.  they can always reapply.  Github shows all activity.

### Agenda Item (Ad-hoc Topics) - Naomi
* Mascot Challenge - its going pretty great.  We promoted it on social.  Our social person started promoting it last week or early this week and will continue to do so until we close.  We got squids, otters, drop the idea.
* Joe:  The goal is that we don't have someone submit the final one, its more submitting ideas.  LF marketing will turn it into something appropriate.  May is going to send out socials with examples from other open source projects.

### Agenda Item (Ad-hoc Topics) - Joe
* You'll notice I put early september as the deadline for the splash screen.  really want the mascot on there.  Mascot Decided on, marketing has its thing, etc.  We have 2 months to get thru that entire process.
* Colinb: If they're AI submissions, you probably are going to need to talk to an artist?
* Joe:  no matter how its submitted, even if truly hand drawn , its still going to go thru our internal marketing and approvals, and all taht, copy right check and all that.  the endresult is going to be more stylized for O3DE.  All we'rel ooking for right now is the idea.

### Agenda Item (Ad-hoc topics) - Joe
* Everyones out 4th and 5th.
* I'll be at Siggraph at end of july
* I'll be in hong-kong for open source summit late august
* I'll be on PTO for a week in september.
* Then we have RosCON, towards th end of october
* Basically out a week every month to sell the idea of O3DE to as many people as possible.

### Agenda Item (Ad-hoc Topics) - Nick L
* Updates for actors no longer crashing.
* Some actors have weird bone positions, and may need post-processing.
* In crytek, Z was up, instead of Y up, and characters run around on the XY plane.  thats just not standard compared to game engine.
* All otehr games is XZ, Y is up.
* null:  Emfx.

### Joe:  Other open source stuff?
* Mike is setting up LFS and teaching us how to do LFS on the repos.
* Starting with startergame. G et those assets up.  Got a contributor who is just waiting for the LFS endpoint
* next is Nemo (underwater demo).  Get those in
* Then Beach City / Crusoe
* Agreement with AMZN is that they have to initially be hosted under the O3DE Repos.  Once they're there they can propogate and  anyone can do it from there.
* The crucible assets are terrabytes, can't be easily committed like that.