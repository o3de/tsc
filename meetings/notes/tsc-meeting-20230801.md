# TSC Meeting - 8/1/2023

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L 
* geds-dm [Amazon]
* Colinb[APMG]
* Nicholas [Red Hat]
* null [Amazon]
* RoddieKieley [Red Hat]
* Naomiwash
* Sid_Moudgil
* HighFly [Fly Forge]

## Agenda Items
https://github.com/o3de/tsc/issues/90

This is a regular O3DE TSC meeting.  The agenda had no items on it.

## No-Code-Project trip report by Nick_L

so trip report from doing a no-code prototype project: works pretty well, but somethings dont work

Things that don't work and will need more intense engineering to solve
* you cannot modify the active gems because it doesn't actually run all the cmake target stuff that knows what dlls are made
* some gems, even if precompiled, do special things in their cmake files (for example, register python requirements.txt).  This will not function since those scripts don't run.
* You cannot create a default game monolithic launcher and there is no generic launcher

## Naomiwash - Howto SIG and DOC management
* moved it to the wiki

Another doc:  How to maintain the roadmap doc. 
Anyone opposed to moving it to the wiki?

## GPU Stress Testing - HighFly [Fly Forge]
* Loft example has a lot of GPU stress
* MP demo has the best representation of an actual video game
* MPS is probably the best balance to stress both.
* MPS has high RAM requirement.  
* Min spec is 4gb - but MPS takes more.  Streaming textures is enabled for vulkan and dx12. You can set a budget.

## GPU Budgeting (Sid)
* Theres a cvar that controls the total budget that the renderer is allowed to use for textures.
* It will dynamically scale in and out mips to satisfy the budget
* A new system is coming that will automatically set cvars based on hardware detection, which would allow auto configuration of any cvars.
