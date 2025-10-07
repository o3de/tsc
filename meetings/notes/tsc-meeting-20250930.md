# TSC Meeting - 9/30/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L. A.
* colinb[APMG]
* hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* jayrulez
* Joe Bryant [O3DF]
* JT [SCB_GameDesgin]
* Luis
* Naomi WAshington [LF]
* Matteo [Loherangrin]
* Nick_L
* null
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Release soon - are people testing it?
* We are not sure that people are testing it.  We're not seeing a lot of exceptions.
* Joe will talk to marketing about download volume.
* Joe:  people are downloading the installer for stabilization, I've had to help people with them.  I just don't know how many.
* Joe:  Ping Mike-Chang for sig release, ask how many.  Its the best indicator we have at this point.
* Steve P [Amazon] - debian package is 40% smaller.

### Announcement - Jan Hanca - we talked about backporting some gems to 2505, o3de-extras.
* As we explained, we back ported some gems to 2505 we think its nice if we release it.
* Everything in the engine already, allows us to do that, we'll release backports for ROS2 gme and Simulation-Interfaces Gem.
* it will be included in repo.json and updated on canonical repo.  So we don't have to do it 2 times.
* Joe:  Good for enterprise that does not upgrade very often.  Let me know when you guys advertise out that you've made this change
  and I can ask the foundation to piggy back on that, as well, that our newest ros is compatible with previous versions of o3de.
* Jan: Definitly for the future we should think about it in terms of versioning, we changed the major for both gems in 2510, so in
  2505, we can still stick to changing a minor revisions.   In the future it might be impossible if we want to backport something.

### Discussion - installer post-build steps
* Nick L: code already exists in project manager to try to install python as well as run the requirements.txt scripts.
* So removing the requirement to do so (or roll back) in the installer was not fatal, it still tries to do it but no longer in a situation
  which causes complete rollback.   It shows a dialog and helpful log even.

### Discussion - Cmake and ubuntu 22.04
* Ubuntu 22.04 users will need to fetch latest (or > 3.24) cmake
* we will need to provide instructions on this.

### Discussion - ciso646 and physx issue (Nick L)
* Nick: Physx 4 is going to be difficult to build its getting so old that it is no longer compliant with clang20 and other compilers.
  Building it with old compilers is still possible, though, but that's a lot of work for all the platforms (ios, android, pc, linux, etc)
  to get where we are now that takes away from us doing other things.  Perhaps we should drop 4?
* Can we move to physx 5 only?
* null: No arm support, no neon/etc, no ios, physx5 was not an open source drop in replacement, there were some hefty tradeoffs in physx5
* null: I recall really struggling to get it to build on all platforms.
* Matteo [Loherangrin] - There is a version of physx5 in our scripts - still pulls upstream repo.
* Matteo - maybe our fork was only used for.

Joe: Please make a priority to fix anything in the release.

### Discussion - No dependency system in cmake
* https://github.com/o3de/o3de/issues/19199
* We don't currently have a dependency resolution system in cmake configure at all, so if a gem says it depends on another gem,
  its not going to automatically include that other gem in the build.
* It uses resolvelib.
* null: autogen is python.

### Discussion - Versioning Document
https://github.com/o3de/sig-release/pull/354
