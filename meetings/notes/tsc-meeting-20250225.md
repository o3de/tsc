# TSC Meeting - 02/25/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* JT [SCB_GameDesign]
* Nichal Pelka [Robotec.Ai]
* Naomi Washington
* Nick_l
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Sid_Moudgil [AMzn]
* Steve P [Amazon]
* vfxno

## Meeting Notes

### Announcement - none

### Discussion - Sid_Moudgil [Amzn]
* Leak related to the use of resourceviews in general
* Pinged Huawei and they are looking into that leaks.
* Dev branch is a decent place except one leak that was found related to views. GHI exists.
* Galib is looking at removing HPHA and see if that is more stable or less.
* We talked about the HPHA and how that we should be dropping pages, etc...
* Robotec.AI found a leak thats not in the dev branch - in  their use case, there's a thread for it
  Its in the GHI.
* A very large level like startergame and it takes more memory.
* There are ways to specify how many mips to load at distance but streaming textures is enabled and works currently
* Streaming geometry is not currently supported.  The GPU understands it all properly because it uses tiled memory.
* Texture can have 5 mips and each mip can have 200 blocks split, you update the references to the block.
* (Sid) We would check the persistent cache, first, then reuse them.
* (Sid) transient views are created every view.  They removed the persistent cache, so we would never check it.

### Question - JT
* Joe has 90mph winds, anyone heard from him?
* Naomi:  Talked to him last night - likely his power is out, 90mph winds.

