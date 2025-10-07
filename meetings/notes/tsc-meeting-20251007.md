# TSC Meeting - 10/7/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* hellaenergyh (Nick) [Red Hat]
* JT [SCB_GameDesign]
* jayrules
* Matteo [Loherangrin]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Naomi Washington [LF]
* We have splash screens from the competition entry and will have something for you for the release.
* (Nick) Let's go find out what went wrong with the splash last release.

### Announcement - Hellaenergy
* No more changes to stablization after this friday.  No more changes.
* (No replies)

### Request - Hellaenergy
* Can each sig give us a highlight paragraph for the release?
* Please respond on the release note issue.  Review your section and provide a fancy highlight.
* Friday 10th is freeze.
* https://github.com/o3de/sig-release/pull/357

### Discussion - Phyx4 + Physx5
* Nick updates on physx
  * Physx5 seems to have all the platform acceleration that physx4 does (ARM NEON, etc)
  * Our fork compiles physx5 for all our platforms (Win64, Linux Aarch64, Linux x64, Ios, mac, android arm8 64)
  * Our fork compiles physx5 WITH GPU / CUDA but our engine doesn't use it, and we can't really support it
    due to EULA/LIcensing.  We will remove the GPU support but allow people to grab and get it themselves.
  * Our fork is old, but the newer version of physx5 significantly diverges from the old one which was closer
    to 4
  * We should deprecate physx4, then upgrade to latest physx5 (do not try to upgrade and deprecate at the same 
    time)
  * Building physx5 is actually very easy, they have a PAL like layout where each platform has a folder containing
    an xml preset file and then CMakeLists.txt for each sub project (ie, vehicle2, pxfoundation, etc).  Those cmake
    files only contain overrides, so they don't have to control the entire build, just what flags to set for those
    targets, specific to that platform.

* Matteo [Loherangrin] - robotics might be afflicted by latest verison
* Steve P - we might have to make a tool to migrate  All the serialize data, component setups, etc.
* colinb[APMG] - We should consider giving the user a long a runway as possible.
* Matteo - I don't want to scare users.
* Colinb:  physx is hte only gem that contains a pattern that's ideal for gems - it reaches into another gem
  from that gem, which is kind of against the rules.
* JT: Jolt intgration - extensive bullet physx bullet experience, I've looked into Jolt before, looks like a good job
  and hopefully that comes on board soon.  HOpefully soon we can get a bullet physx engine gem, next year, hopefully
  we can get desructible physics for 2026 second major release.  If not we have a tool to use it externally and bridge
  the data into open 3d engine, support for other physx engine, and thus more havin a uniform setup. 
* JT: With a particle system, I created a stub pr with documentation to put in, I need to tack it in and it should be
  up after the release and finish that up and we can start documentation in the development branch.
* Nick L:  We might need a nice sample repo for some good particles
* JT: I'd like to factor out some of the popcorn FX and bring in open particle system, and it will be a good community.

### Discussion - Versioning Document
https://github.com/o3de/sig-release/pull/354

