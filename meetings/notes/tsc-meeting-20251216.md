# TSC Meeting - 12/09/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]


## Attendees (By Discord name)
* Andre L. A.
* Arbiter
* colinb[Apmg]
* Hellaenergy (Nick) [ REd hat]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P. [Amazon]

## Meeting Notes

### Announcement - TSC Meetings are over for this year.
* Most sigs are not having meetings until new year.

### Discussion - Joe:  Question for sig release, hows the docs?
* Jan Hanca:  I checked the PR for release, there were some problems, changes made for 25.10 but reverted
* I created a PR to his release branch that fixes it.  As soon as I get these approved, I'll apply them
* issue: We didn't cherry pick main to development.
* when JT cherrypicked from development to main, lots of merge comments.
* We need someone responsible for every repo, to do that.

### Discussion - Mike C:
* Did anyone have issues with visual studio 2026
* No issues reported

### Discussion - GHA over to github
* 80% cost savings, and the remaining bills are for LFS.
* 60/40 AR to CDN
* If we enable LFS for all archive releases, it will try to download all LFS items.  One pattern is
  that people download a zip file for CI/CD systems and that incurs a lot of traffic.

### Discussion - further automating the docs release
* Joe: Request from my side is as easy as possible for a person to submit documentation.
* Right now its convoluted and complicated.
* Colinb: Is there docs around jenkins, do we even want to release it?
* Mike_C there is a RFC for the GHA flow inside the sig build repo, in the rFCs folder.  We don't have a 
  like for like flow but I can work on expanding that documentation for later.

### Discussion - JOLT and deterministic physics
* Jolt fits the bill perfectly for that, user "cheddaspice" is working on it.
* Joe: Perhaps SIG-Sim can have a rough timeline.  Maybe not exact, but by Q1 would like to have a
  coherent answer for that.
* https://github.com/nick-l-o3de/o3de/wiki/Particle-System-Todo
* Hellaenergy: Do we have any relationships with academic or institutional?  Would they be interested?
* Joe: RIT has been using it in the past, but the main contact retires at the end of this year.
* Joe:  Would have no problems with a university team working on a project

