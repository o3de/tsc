# TSC Meeting - 2/17/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* Cheddarspice [iamjbq]
* Hellaenergy (nick) [Red Hat]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* nanayellen
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Steve P [Amazon]

### Announcement - SIG-Release - Matteo
* We are going to start the stabiliation process for spring, next wednesday 25th, we are
  going to create the stabilization branch and will write in Sig-All when everything is created.
* We should probably defer Qt6 and Localization for next release.
* OpenParticleSystem is going to be released as preview
* Perhaps we should ask for feedback as part of this release?

### Announcement - Mac Port - Steve P [Amazon]
* 95-99% thru, would merge it into the Qt6 branch.  
* One issue I can fix - 3p package wasn't formed properly, but the ones that have been
  problematic is the fixup bundle issue, rpath with qt6 3p package, and allow others to contribute
  to it.
* https://github.com/o3de/o3de/pull/19567

### Discussion Topic - Qt review strat?  Localizaiton review strat?
* 1500+ lines of code pending merge, its going to be a huge merge issue.
* We are going to have to lean on UI test

### Discussion Topic - i18n PR
* https://github.com/o3de/o3de/pull/19554

### Discussion Topic - Physx4 removal
* We can message the release note in spring, and say we'll remove it in october, if there are some problems.
* 3 things to announce that are deprecated / impact:
  * Qt 6
  * PhysX4
  * CMake?
  * deprecate vs2019

* JT: We need to get back in the habit of making an issue in the repo for it.  we used to do issues first,
  and we need to get back into that habit, making sure that there's an issue for this stuff they can search
  for it and find it.
* Ninja packaged.
* short transitional periods we would roll it forward.  Support transitional period.

### Discussion Topic - MPS / WWISE / PopcornFX (Continued again)
* DELAYED FOR NEXT WEEK