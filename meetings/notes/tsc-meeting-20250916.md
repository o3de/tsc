# TSC Meeting - 9/16/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loharngrin]
* Nick_L
* null
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Matteo [Loherangrin]
* SIG-RElease we are working to collect the release notes. 
* I've written a description but please help check if the details are correct.
* I've assigned each item to the relevant sig, even if there are multiple approvers, please claim the item if you feel it has the wrong
  owner.
* Joe: we need more reviewers to be promoted.

### Discussion - releases compatiblity
* Research ongoing on why the ubuntu 22.x built deb doesn't work with other versions of clang.
* You can use the engine pre-built.   You can make a project against the pre-built newer verisons of clang.  But we're seeing reports
  that ebus messages do not arrive when they should if compiler does not match.  
* Nick: This implies that its a multiple definition issue - that is, when you `BusConnect`, the bus invokes a function to get a global
  object that contains the list of connected listeners and add your listener to.
  Later, when someone `Broadcast`s, the bus invokes the same functionh to get that same list loop over it, and invoke the callbacks.  If
  that context object is duplicated somehow between different modules instead of truly being global, we'd see this behavior.
* null: could it be lambda callbacks changing the way they're called between the versions, its a complex system.

### Discussion - Current State of Particle System
* Needs a lot of testing
* Current PRs are improving it
* People should start reporting / contributing things they think should take it out of preview, blockers, etc.

### Discussion - Steve P
* I've been off and on building 3p libraries for mac silicon.  Long story short a lot of the library versions
  are too old for xcode, so I've been bumping up the versions just as a proof of concepts as to what libraries can be built.
* QT 5.15 cannot be built on ARM architecture.  Guillarme hd been done qt6 update and I can see if build that, these third
  party libraries will need to be updated.  The way I'm seeing it, the mac effort, seeing what versions are available right now.
* Nick:  We want as little maintennence on our heads a possible, if possible, we'd like to only maintain prebuilt verisons of
  the really expensive large co-dependent libraries like Qt, QtForPython, and Python, for example.  If possible, it would be nice
  for the rest of them to be FetchContent Libraries
* Jan:  Could we maybe move http://sdformat.org/download to use the built in one?
* Nick: Yes, we should use the operating system version wherever possible rather than being responsible for shipping it ourselves.
* Nick: I would recommend fetchcontent wherever using the built in OS version cannot suffice, and only making prebuilt packages when
  we have to.

### Reece H. [DrogonMar]
* Spatialization for Audio using SteamAudio.  It is not an audio playback engine, just spatializes and creates buffer data.
* SteamAudio already has examples, knows how to deal with it, support it.
* Using WWISE or FMOD it has support for those.  It could be compatible with WWISE or updated for it.

### JT - Docs team is considering using ADR (?)
* See link in the Sig-All.

