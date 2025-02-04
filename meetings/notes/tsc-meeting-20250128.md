# TSC Meeting - 1/28/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L. A.
* colinb [APMG]
* Jan Hanca [Robotec.Ai]
* Joe Bryant [O3DF]
* Nick_L
* null [meta]
* RoddieKieley [Red Hat]
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Joe Bryant
* Plan for the exact date for the point release
* Start planning for full release in may set up
* Something that keeps coming up is C# support and they want to be able to have their
  engineers seamlessly move over.
* Some companies still having issues installing o3de even with the offline installer.  I'll talk with mike about why that is
  (This morning, Siemens, it failed to install).  I'll do some research and head up some of those efforts.

### Announcement - Nick - ASAN
* ASAN rapidjson

### Discussion - FetchContent vs 3rdParty
* We had a discussion about using FetchContent (which fetches source code or artifacts from a git repository)
  vs using the O3DE 3rdParty system (which fetches zip files from a CDN of prebuilt binaries).
* Nick L suggested we use fetchcontent preferentially, for sources that are small, or header-only (so low compile or no compile)
  and do not require extensive patching or changes.  For other things, we should fork it.
* Nick L noted that fetchcontent has an issue with patching.
* Colinb - One problem is that the engine will stop working if git repos involved are dead.
* We could mitigate this by pulling either from github (in which case, it only dies if github has) or further mitigating it from forking
  locally
* Its also possible to build a hybrid where it can fetch from either.
* Nick L plans to do it for RapidXML, GoogleMock/GoogleTest, and RapidJSON.  The Rapid* are header only, and GMock/GTest compile in a few seconds.
* There isn't a pressing need to try to start an initiative to visit all 3p, but recommend instead, next time a small or header only
  3p needs an update (for example, for security updates) we switch it to fetchcontent if we can.

### Discussion - Qt version
* Colinb - are we going to upgrade QT?
* We would like to upgrade Qt.  But someone needs to do the work, and its unknown.
* Main blockages are the docking system upgrades would either need to be ported to the latest qt, or removed and the system implemented
  all over again on top of hte latest qt.
* We welcome a RFC and effort to do this.

### Discussion - Engine Rearrangement
* Colinb - we should consider, long term, rearranging the engine so that it is more modular and similar to other repos of o3de objects.

### Jan Hanca [Robotec.Ai]
* Plans to do the job of moving some of the gems to o3de-extras...?
* We have plans, but none are currently in motion.
* null - Need to move this all into RFCs.
* good changes but will introduce churn and instability.
* Need engineers to implement and support customers and fix maintennence issue


