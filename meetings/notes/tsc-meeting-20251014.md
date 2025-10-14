# TSC Meeting - 10/14/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* hellaenergyh (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* jayrulez
* Matteo [Loherangrin]
* Nick_L
* Sid_Moudgil [Amazn]
* Steve P [Amazon]
* Tobias Alexander Franke [Huawei]

## Meeting Notes

### Announcement - Hellaenergy (Nick) [Red Hat]
* Release of 25.10.0 - tomorrow 10:30am

### Discussion - Android 16k page size support
* November 1st deadline
* https://discord.com/channels/805939474655346758/816043694762754088/1417938656609698014
* r27+ android NDK is required.

Requirements:
* API 34 or higher
* NDK 27+ (Clang 18) with compile flags
* see https://developer.android.com/guide/practices/page-sizes
* https://github.com/o3de/o3de/issues/19294
* Carbonated has already done this and is willing to share their work, but they don't have the time to
  merge.

### Discussion - Fast Math
* colinb: INF/NAN are debugging features.  Fast Math shoudl be off by default, those should be available, and how you find 
  those bugs in your code.  OFF by default is the right code.  OFF by default in release.  Having it available for people
  to turn on for a release would be something people might want to do in certain situations.
* colinb: That code will be able to sneak past AR if we have it.
* colinb: The delta in precision is not very high, it does become much more significant the number are further away from zero
  and they become much more noticable, if you have a really large world.  You'll see stuttering and stuff sooner than you would.
* Decision: We'll turn fast-math off - by default - but keep it available to turn on.  If you turn it on, there will be NO
  checking for infinity or NaN, that code will be removed by ifdef, since it is meaningless.


