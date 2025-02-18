# TSC Meeting - 02/18/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Nick_l
* null [meta]
* Reece H. [DrogonMar]
* Roddie Kieley [Red Hat]
* Shauna [Genome Studios]
* Steve P [Amazon]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Joe
* 24.09.2 Tuesday 25th - Release folks attend
* Release notes done.  Posted on release-sig
* After today, no new PRs in without exception.
* After that we have to start with release branch for next release (Official May Release) the day after we release 24092
* We will need Nick L to create the PR to promote it to main.
* Jan:  No PR after today? I have one thing that has to be changed, for sure, we didn't increase the version numbers yet in the gems.
  ROS2 Gem version needs a bump
* Steve P: We also need to create a release zip for the new version - the new zip file for the gem.
* Github has a limit to size of repo but not to releases.

### Discussion - Joe
* Joe will be very busy at conferences in March.  Attendence will be poor.

### Discussion - Asan + stl::vector
* Nick explains how the current implementation of OpenMesh allows a stl::vector to cross module boundaries
  causing some of the code involved to compile against VS2019 without ASAN and the code in the engine 
  to compile against whatever VS you have, with ASAn if enabled.  This causes mismatches between STL annotation levels.
* null - We need to isolate the use of stl api boundary across unknown representation.
* null - another option would be to create a wrapper library around the OpenMesh library that does not expose
  that particular object across boundaries.
* Current plan:  Compile OpenMesh with the engine itself, failing that, rev a new package that is in 2022 + ASAN.



