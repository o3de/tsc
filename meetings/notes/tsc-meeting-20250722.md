# TSC Meeting - 7/22/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.Ai]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike Chang [Amazon]
* Nick_L
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Sid_Moudgil [AMzn]
* Steve P [Amazon]

## Meeting Notes 

### Announcement - Hellaenergy
* Looks like we're on track to release today.  We'll be doing it async
  within SIG-release's chat.  We have 1 need for a PR, in the TBD
  in the list.

### Discussion - QT and wayland native widget stuff
* The moment a native widget gets created, everything stops working.
* https://gitlab.com/wireshark/wireshark/-/merge_requests/11702
* (Discussion on Qt wayland compositing and source.)
* Its possible we should wait for qt 6.x support before we push hard into
  wayland, work with QT 6 whenever we get that working.

### Discussion - Mike Chang - CMake XCB.
* Going to make to bump cmake to 3.27, 3.28 likely.
* We need to support X11 namespace for xinput and a few other things.
* Take advantage of a few things that might be relevant
* 3.28 is 24.04 LTS.
* 3.22 on 22.04 LTS.

### Discussion - Engine and Object Versioning
* We need to maintain and take verisons seriously
* Jan will continue working on the RFC.
