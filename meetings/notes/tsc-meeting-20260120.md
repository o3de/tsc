# TSC Meeting - 1/20/2026

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Arbiter
* colinb[APMG]
* Joe Byrant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Steve P [Amazon]

## Meeting Notes

### Announcement - nick - The Parent / Child Activation system is now merged in
* Nick: The parenting / entity actvation code is now live in `development`
* Joe:  What if they use the existing activate/deactivate in their project?
* The old Activate / Deactivate functions are still there, and still explicit and will still
  activate and deactivate entities without checking any other conditions, like before, but the new APIs
  can be used to activate conditionally based on parent state.

### Announcement - Joe - Connect meeting tomorrow 8am PST.
* Just a short update on whats going on.

### Announcement - Matteo
* We have started the work on 2nd point release.
* Just a .2 release for fixing the vs bug.
* The release date will be in 1 or 2 weeks.

### Discussion - Deprecation of Cry*
* CryQuat, CryMatrix, etc.

### Discussion - Support for Mac
* Any update?
* Arbiter: Its improving.  It compiles but does not run
* Steve P: I've been putting up packages.
* Talk to guillarme about update to qt6.
* whoever wants to take point let them know the situation

