# TSC Meeting - 8/26/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Hellaenergy (Nick)[Red Hat]
* Jan Hanca [Robotec.ai]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Nick_L
* Naomi Washington [LF]
* null
* Reece H. [DrogonMar]
* Shauna [Genome Studio]
* Steve P [Amazon]

## Meeting Notes
Before the meeting started, there was a brief discussion about find package and CMake.

### Announcement - Naomi on behalf of Gaian
* We are doing another revamp of the discord server
* Gaian is taking the lead, they have a proposal in place.
* They've already asked you all feedback, and we'll start renaming things, channels being consolodated, that kind of thing
* We'll let everyone know in the announcements channel.

### Discussion - Miniaudio
* Miniaudio has been updated.
* Matteo : We should evaluate whether we want to put it in the upcoming release.
* https://github.com/o3de/o3de/pull/19195

### Discussion - Open Particle
* https://github.com/o3de/o3de/pull/19213/files
* Particle System for the editor.
* null - the ATL concept comes from wwise - some of the plumbing we need to make that nice 
  Very large difference between streaming audio, stingers, audio localization, and so on.
* Perhaps we can make a feature branch, or a different repo for this kind of thing?
* Colinb: from the perspective of hardening, keeping the core as minimal as possible, a particle
  system that is probably core, but in the future we should have maybe a more formlized way to getting
  things like this into the core.

### Discussion - Engine versioning
* https://github.com/o3de/sig-release/pull/354
* Patch versioning nightmare scenario - perhaps we can use version ranging?
* When the merge goes in, it gets incremented again.
* colinb: For example, there is a lot of time between AR going in.
* Jan Hanca - Multiple repos with different gems - we either link to a full stable release, or we link
  to a commit or build from a source.  From that perspective I don't see any reason to update a patch
  on the development branch.  I don't see a reason to pump the internal reversion.  For the releases.

