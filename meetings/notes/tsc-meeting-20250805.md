# TSC Meeting - 8/05/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Nick_L
* null
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes 

### Announcement - Joe
* I'll be out Aug 10 to Aug 26.  This is my last TSC meeting for august.
* SAme thing for the SIG-Release meeting, last one for august.
* I'm still reachable for emergency via discord or email.  I can still check that - where I will be there will not
  be enough bandwidth for voice or video so text messages are the best way to get ahold of me if needed.
* I'll check once per day while I'm out but that's pretty much it

### Announcement - Joe
* Siggraph has a lot more interest in O3DE this year compared to last, lots of meetings being set up, which is nice.

### Announcement - Joe
* AMA - September, if there are questions you have that are fairly complicated that you want me to answer the AMA
  then please send them ahead of time so I can do some research.

### Discussion - Release Versioning Strategy
* https://github.com/o3de/sig-release/pull/354/files?short_path=266993c#diff-266993c75289497846fa885c55a2cc1755c7e6b7c0139c0fa326a04c9831de08
* This document starts a discussion, not to give the answer.
* One issue is that you can't link to a specific version of a core gem.
* Joe: Tangentially, I'd also like is to solve:
  * Right now, when you install a new version of o3de, you have to tell your existing projects to upgrade to a new version.
    Its not in your face on how to tell your projects to use a new version.  You have to go into the project setting / engine setting, to
    point at the new engine, else your project will launch the old engine it was using at the time if you still have it installed, if you dont
    have it installed it just errors.
  * Make it more intuitive for users, maybe there's a way to update them.
* Matteo - Another option is to split the projects that are displayed int he proejct manager - one for current version, and one for older
  versions.  Current project only shows= projects that are related to the same engine.
* Joe Bryant - For example if I'm working for EA and I am the lead tech for that team and I'm the one upgrading for newest version, which
  is very common, different team members or roles are on different versions.  Small teams running on old and new versions, even one or two
  version behind.
* Youd have a small group that would have the latest and greatest and test it out before we distributed.
* Was the hardest when we upgrade from 32 to 64 bit, various groups on different versions.
* They may have to install various versions of the engine since they are releasing projects and some may be in lockdown ready to release.
* colinb- in schema2 you pick the engine via a version string, name, etc.  It can be matching == or greater equals, etc.
* Joe:  Plans for auto upgrade, it needs to be a non-destructive process.  Copy the project for the new stuff, do the conversion there, 
  see if things work.
* colinb schema2 sees what schema version you're using, makes a new one right beside it with gem2.0.json for exmaple.  When the system is
  written it looks through and looks for the 2.0 json if you have one, if it doesn't  it falls back to the other one.  it doesn't destroy
  anything, its up to the user if they are happy with the new changes they can rename the 2.0 json to gem.json.  Its all file based and
  a user's choice at that point.
* colinb: we shhould not try to assume the project manager is associated with the engine in any way, we should not perpetuate that pattern.
* JT: I assume with our growth we're seeing, we're getting engine testers, we'll see engine testers increase, and they do have specific needs.
  Engine Testers:  Someone testing a possible new engine for a project.  Engine evaluators sometimes.
  Early people, like, one person assigned.  I've worked with them out of the north county San Diego area, we have an annual mixer forum.
  They've talked to me about what they do in that position.  It was referenced earlier.  People are testing new engines, new softwares to
  use new tooling, they'll run the engine they're testing through some ropes.
  If it works with their pipeline, etc.  they have needs, they have anything thrown their way especially documentation thrown their way
  or workflow or stuff in the engine that is very clearly delineated.
* Colinb: last week I suggest even before implementation, we get this stuff down and start using the versioning.  Getting used to making
  changs, and when making changes, update the version, just to get the checkin criteria getting used to it before it becomes a necessity.

