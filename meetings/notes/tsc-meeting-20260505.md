# TSC Meeting - 5/5/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Andre L. A.
* Cheddarspice [iamjgb]
* Christian Hinkle
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* JT [SCB_GameDesign]
* Luis
* Matteo [Loherangrin]
* Mike_C [Amazon]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* xdllq

### Announcement - Matteo
* Today - we are going to close the splash screen contest for the next release
* We got 5 submissions!  They are amazing.  Next days we'll announce the winner.

### Discussion - Matteo - Release
* Propose delay of 2 weeks in release schedule in order to have more time to polish the release.
* As we discussed in the last SIG-release meeting, we have reached a good stability, but maybe some
  extra time can help to have a better result in the community.
* I was hoping that someone from robotec.AI was part of the meeting to discuss directly.
* The idea to delay is also to be more confident also with the robotec.ai part.  If I remember correctly
  they say many times that on ROS there is a big release that is coming, later this month on 22, and
  they have already tried to test all the new stuff that they are release on the pre-release verison of
  ros, but since this is a LTS version, I think that having a testing version of the general version
  could be worth it to minimize the release to minimize the risk after point release.
* We are going to release the week before ROS.
* The process has changed since the previous releases, we have to get involved with the LF Helpdesk.
* We'd like to find more comfortable time for them.
* We feel like the quality of the codebase already is sufficient for release, but its everything around
  that - polishing example codebases, looking for more regression bugs.  The UV Offsets thing was found
  essentially out of luck.  We want to be sure we have no other blocking stuff.  Having 2 more weeks
  can be helpful in order to make a call to the entire community to test the version we have actually in
  the branch.  We need to freeze that version, say thats the RC, and let people report ASAP.

### Note - Hellaenergy (Nick) [red Hat]
* I finished a fedora 44 RPM - ready for using as o3de-stabilization
* I will post once the latest build is ready in copr, testers are welcome and encouraged
* What I'm designing it for right now is to get it into fedora proper.  What I'm doing at the moment is
  pulling out all the packages at the moment that fedora already supports and slimming down the RPMs as much
  as possible.
* I have an experemintal repo where I'm doing a lot of this work.  I'm building those often, or as often
  as I can.  It takes 5-7 hours sometimes.  Wheras locally I can do it a little over an hour.  
* Sidecar project - from the information I'm learning, I've also got a potential flatpak in the works.
  That might be more distro agnostic if people choose that route as well.  it fits in the fedora market.
  We'll proceed with the RPM since we can use it internally.
* JT:  Is there any way to talk to people without discord?
* JT:  Is there anything public facing to link people to, that isn't discord, like,a link to the repo
  or etc?  
* Hellaenergy: copr-project has a homepage, and it points to the repo for this project where it points.
* I also positioned this so we can poistion it in o3de-binaries, and also with some CI integration and
  github actions, and pretty much so we can integrate it into o3de's build.
* In copr, the end-product RPMs end up there, which we could harvest.
* We have licensed it under the same license as O3DE.
* I did pull out as optional, certain packages that did not fall under fedora/copr guidelines for reasons, 
  it won't have any licenses that conflict with copr/fedora guidelines.
* For example, an nvidia one.
* https://github.com/nickschuetz/o3de-rpm/blob/main/FEDORA_ROADMAP.md#restricted-bundles--the-off-limits-four
* https://github.com/nickschuetz/o3de-rpm/blob/main/BUNDLED_LIBRARIES.md

### Discussion - Versioning - Nick L
* NickL: I would like to find the best way to propose getting the engine on the same timeline of versioning. 
* NickL: How can we do it more efficiently.
* colinb: We have to agree on what unversioned gems mean
* colinb: we have to agree on what the defitioning of the format means (major, minor, patch)
* colinb: We need to enforce an upgrading/release strategy.  Just the same as we should enforce that on all
  objects, not just the engine.  Did you change API on the object?  Major/Minor/new object?  Is it a minor
  increment?  All numbers all increment at the same time.  
* colinb: We need to be able to document the changes in the jsons.  The "solver" we use currently, in python,
  resolvelib, needs to be able to come to a solution when you choose a root object, the root object has the 
  version, and we need to have a system in place that describes the dependencies of those objects with the
  version #.  Its almost not enough to say that gem x is a dep - we may have to have a scheme for describing
  the version number in the dependency.


