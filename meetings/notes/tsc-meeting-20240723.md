# TSC Meeting - 07/23/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Jan Hanca [Robotec.Ai]
* Joe Bryant [O3DF]
* Lloyd T. [Carbonated]
* Mike Chang [Amazon]
* Mike S. [Carbonated]
* nick_l
* null (Meta)
* RodieKieley [Red Hat]
* Sid_Moudgil [Amazon]
* Steve P [Amazon]

## Agenda items (official)
Agenda Topic: https://github.com/o3de/tsc/issues/133
(No topics present)

## Announcements / Discussions for everyone to hear

### Announcement/Discussion: Mike Chang - AR.
* PRs in flight to modify periodic builds.  Periodic builds will not trigger if no code change has occurred.
* Originally we were planning to run every week, I'm open to do that, but right now they run daily.
* Nobody seems to be putting up any github issues in regard to anything which failed on Periodic.
* Joe:  move to weekly cadence.
* Mike: It was running daily regardless of whether there's a change
* Joe:  move to weekly - we need to set up a mechanism for people to check for failure and resolve it.
* Mike: We will have a larger discussion about which ones to disable if they're not useful anymore.  Some are vs2019 jobs, or unity vs non unity stuff

### Announcement/Discussion: Mike Chang - Stabilization issues
* I put a solution for the Stabilization branch o3de-extras up, and a PR will come in and hopefully resolve the issue
* We resolved the issue with the one pull request in question that was in sig-build.  I think that is the way forward from there.

## Discussions - Ad-hoc

### Mike Chang - converting to github actions
* So far I can build on all platforms, including mac.
* Its free, but its a limited resource in regards to CPU.
* considering using object caching from certain packages like ccache to cache those objects and reuse them
* It works on a build with no changes, and reduced times from 4hrs to 23 min.  
* I had to change the compilation flags from -zi to -z7.
* Joe:  It will be a presentation to the TSC.
* Joe:  Its pretty slow on Github Actions.  I talked to the board, and the Board is fine with us trading perf for cost since we're cash strapped.  The current AR is a significant cost, its over $100k a year, if it takes 2x as long but its free, then that's a fair tradeoff.
* Joe:  A lot of tests have proven to be flaky as well.  In the interest of having a plan:  Periodic builds ---> Github Actions ---> Tests.
* Nick: Mostly care about the AZCore / basic tests, etc.
* Joe:  Move everything over, then figure out which tests are valuable.
* Sid_Moudgil: Does it support mac?
* Mike:  You get mac, m1, x86-64 windows linux, but you have to pay for GPU and windows-ARM is not present yet.
* Mike:  we might need to hold onto the installer builds for a little bit.
* Mike:  generation of the ccache might want to retain it on jenkins.
* Mike:  I went thru the ccache documentation, and one example of a build with ccache.  They are mostly the same.  22min build step.
* Nick:  you may be able to save time by turning unity off with ccache.

### Joe - I will not be at the next TSC meeting
* I'll be at siggraph
* galib will be giving a presentation on the renderer at 8:30am on Monday July 29th at SIGGRAPH.
* Feel free to tune into that.  Its being presented as part of the "Birds of a Feather" as the ASWF (Mostly about film and video)
* Helps us slowly get us some recognition in that space.  O3DE is an option there.  A little rough but we have things to do, but its an option.
* Please give input about the Particle Editor/Engine.  Its your chance to give input. https://discord.com/channels/805939474655346758/1265005651822645309
* Getting the stabilization to development reverse integration up.
* Joe: Keep an eye on the stabilization thread

### Joe: State of matter [SOM] from RIT is now in Steam
* https://store.steampowered.com/app/2844240/State_of_Matter/


### Joe - Stabilization branch
* One of the things I want to do (Broached with board + marketing) is get Stabilization Branches downloadable from binaries
* Get those installers up so that its a lot easier for people to find.  (I have to find the links and its difficult)
* Proposal is to put a stab branch up and we wanted to figure out how to display it, etc, I just wanted to get it up there to download it, naturally and easily - we have one for dev, now we have one for stabilization.  we have to remove it when we dont' have a stab branch, so there's a little bit of upkeep, but it will make it so much easier, people dont' have to hunt for downloads.

### Joe - WEBGPU
* We are considering WEBGPU, it will open doors for enterprise.
* Sid_MOudgil: need a shader pipeline for WGSL, and its insane on Unity.  HLSL->GLSL->SPIRV->TiNT->WGSL. We can add a pipeline, but its a new platform, so it impacts not just the renderer, but the runtime, disk memory, memory usage.

### nick - remember to pick into stabilization!
