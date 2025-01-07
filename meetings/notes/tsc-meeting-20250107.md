# TSC Meeting - 01/07/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Guthrie [Amazon]
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Naomi Washington
* Nick_l
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* Tobias Alexander Franke [Huawei]

## Meeting Notes

Happy new year!

### Announcement - Joe
* Sig-Release voting for SIG-Chair
* Joe will still be involved, and I will happily coach and train whowever decides to pick up that position, but cannot be the point person.
* Joe is travelling a lot, and will become a major bottleneck for releases.  As an example we want to do a point release but January is off the
  table because Joe is travelling so much in January.  Travel ramping up a lot is good because it means we can get more foundation members in, do more
  things that we currently cant, etc.
* Talk to Joe or nominate yourself.
* Joe will be at the Connect meeting on the 15th talking about 2024 retrospective and talking about 2025 moving forward, and will unveil the roadmap so far.  One input I need is how to best post the roadmap in a way that is actually usable by people.  I did it in github last year, website seems to be easiest, but I need to get feedback from people.
* Next week I'll be difficult to get ahold of on thurs 9th especially.

### Discussion - Jan Hanca - Robotec.AI
* Progress with change of tests to github actions.
* Actions is a little slower but much, much cheaper.  Mike is working on it.  (Not currently in this meeting)
* Goal was to get it up this month, fully in.  He's been testing it for several months now.
* Jan Hanca: We want to be ready for a full release or point release and were thinking of auto tests in the ROS2 gem, and this happened already, we don't want to repeat it.
* Joe: I recommend reaching out to mike.  We do contract Mike.  It is okay to reach out and specifically ask him, how to guide us.  He's building documenation on how to use github actions and the transfer.

### Discussion - Sid
* We are moving all the AWS gems into the AWS repo
* There are gems, and they will live in the AWS repo.
* Gene is looking at a bit more testing, then make the final commit/push that will remove the AWS gems.
* We haven't solved the discoverability yet but they need to ask around and discover them, since they won't show up
* I've also asked Gene to add the Umbra gem (which is being opened sourced).  For the SDK you'd still ahve to reach out and get the actual SDK you could
  get the umbral gem if needed.
* Core repo should only have 2 pipelines - PC, mobile.  Maybe not the AR/VR.  Perhaps the rest can be pulled in from a Gem.  More for organization.





