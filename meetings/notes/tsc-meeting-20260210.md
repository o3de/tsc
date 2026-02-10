# TSC Meeting - 2/10/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* nanayellen
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* SidMoudgil [Amzn]
* Steve P [Amazon]

### Announcement - Hellaenergy (Nick) [Red Hat]
* Officially going to start planning 2026.05 release.
* We have created a new key information document behind that.
* https://github.com/o3de/sig-release/issues/367
* targetting May.
* Mike_C - Do we cut the branch now?

### Naomi WAshington - [LF]
* Moved connect meeting from tomorrow to next wednesday.  Andre is going to tell us about the game jam.

### Discussion Topic - CMake Versions
* Steve P / Mike:  Deprecation methods are being sent out.
* Is there a reason to pin it back to the minimum version or make it uniform across all versions?
* Installer has to update to 2026 without it.
* Be less rigid about it, and 4.1.x and above?  If its not building for you, update to the newest version.
* Arch doesn't have an exact package for CMake yet.  Red Hat can install the latest version as well.
* We do need to ship with cmake 4.2.x at least for windows.
* Redhat 3.30 - we should probably say "we test with 4.2.x and if you compile with a lesser, we print
  a message" but have a minver 3.30 in the code, and ajdust the policy for fetchcontent.
* Use the builtin cmake for project manager builds.
* Jan Hanca [Robotec.Ai] - We should consider the version of linux that is officially supported.  Currently
  we run it and test it on ubuntu 22.04 (previous LTS).  24.04 was LTS release, and next one is released
  this april. We should drop 22.04 LTS since we support previous 2 releases.
* Last time I was updating the docs I fixed it in a couple of places and stating which cmake it was used and
  which verison of ubuntu was used.

### Discussion Topic - i18n PR
* https://github.com/o3de/o3de/pull/19554

### Discussion Topic - MPS / WWISE / PopcornFX (Continued)
