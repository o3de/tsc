# TSC Meeting - 10/22/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Guthrie [Amazon]
* JT [SCB_GameDesign]
* Lloyd T. [Carbonated]
* Mike Chang [Amazon]
* Mike S. [Carbonated]
* Naomi Washington [LF]
* Nick_l
* null [Meta]
* Sid_Moudgil [Amzn]


## Announcements

### Announcement - Naomi Washington - ROSCON
* Joe, Roddie, Steve at ROSCon this week.
* Joe has found out that a lot of companies working with O3DE that he was not aware of
* Naomi posted a video that was part of o3de-connect to youtube about render features/updates
* Blog was created to note the release notes.

## Official topics

### Discussion - Mike Chang [Amazon] - Building using Github Actions (RFC)
* Most of what we have in AR can exist in Github Actions
* Slower than AR - 4 cores, 100 gigs of storage (16gb ram)
* Support for Ubuntu, most supported versions of windows, last 3 versions of macos (not building AR on macos yet)
* We need to use some sort of caching mechanism for build speed.  We're using CCACHE for that.  In order for windows to CCACHE properly, certain compiler flags need to be turned on.
* For linux/mac there is standard compiler flags to use ccache as a wrapper
* There are some things that we need to do, to reduce build output (100gb limitation)  some of the linux builds exceed 100gb, will have to do something about that.  Reduce Debug Output, etc.  Profile builds outputs a lot, need to reduce that.
* Some of the tests I've been working on seem to a lot more time to go thru due to unknown issues (cores? temp files?)  I've posted tests.  They do temp file manipulation and check if files are added/removed.  
* In terms of a plan of what we'll be pushing AR, the goal is to get this working for dev builds, to run in parallel with AR with jenkins, as we gain more confidence, and don't encounter edge cases, we can start moving them into the PR space for approval.  Given they are github actions they will be available in the PR as the actual status.  
* The other benefit is that if they fork the repo they can take the github actions into their repo and execute them locally on their fork, without having to deploy VMs on their local machines.
* It does not cost anything at all, github actions on open source is free.

* Investigate Asset Server Crashes.  It wants to process the timestamps.
* Lloyd 2 issues - file hashes parameters - made it slow
* Lloyd: AP would crash deep inside threading, also.
* Colinb: Please report those if it works.
* Mike Chang [Amazon] - if you zip it and don't preserve timestamps, use the timestamp in tar.
* Next steps - PR targetting dev branch to have it running in the background of dev push.  we'll inspect the output, work on any bugs that arise from that, reconvene.
* Sid_Moudgil [Amzn] - We have to provide a business justification to get AWS credits.  Its a huge cost.  If we can just use GitHub actions we can remove tests or are erroring thats a better approach.  we have access to macs as well and over time we could add mac to the pipeline.
* null - We have a whole team spinning up that may integrate o3de with build system called buck2.  Distributed open source build system.  https://buck2.build/  - backend for cmake, what it would look like to maintain buck2 builds, etc.  Looking at a number of options.
* null - Integrates with meta monorepo, all distributed, it will do the distributed build stuff, any sort of tips/tricks/best practices for managing this conversion.
* Mike Chang - Buck2 is mostly agnostic, rust based, etc.

* colinb[APMG] - Extras?
* Mike:  Extras are not currently being pulled in.  You can do the whole download multiple repos at the same time, merge them together, etc.
* Mike:  Jenkins didn't support multiple repos, but actions does.

* LFS: Mike - O3DF has free credits for LFS.  We'd have to re-commit all of our LFS into github.  Scaler feature maybe?  Commit binary files where you don't have to pull, where you only pull what you need from the head revisision into your git folder.
* Current Use-case for now lets try to get it into AR. We could scale it out into forking and building other projects.
* Mike Chang: Large assets like this, maybe there's some other way to store them?

* RFC for removing the objects from the engine, it would be different from removing the automated testing projects, there are AR implications.

* Is there a tutorial on how to use O3DE with just C++?
*  Naomi:  Got a lot of questions about this, but I don't know where this exists?
*  Joe was going to mention during our Governing Board Meeting we need to be mindful of old O3DE content.  Tutorials / sessions from O3DECon.  If you are aware of something that is no longer valid we need to take down, let us know.  We are getting a lot questions.
* JT: This is a field I'm aware of, universities teach purely in C++.  This is waht some of these students come out of college knowing how to, they need those tutorials.  They have a volume of books for decades on C++ game dev, ecosystem, workflow, etc.
* JT: Keep that in mind.  It may not be relevant in mind to how people here use the engine.  This is the legacy of game industry/game engines.
* colinb: Do the exact same thing in C++ as you do in LUA / SC.





