# TSC Meeting - 2/03/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* Andre L.A.
* Hellaeenergy [Red Hat]
* colinb[APMG]
* Job Bryant [MotBry Entertain]
* JT [SCB_GameDesign]
* Nick_L
* Naomi Washington [LF]
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - JT - Pasadena Booth approved at So Cal Linux Scale (In Pasedena)
* Heavily promoting O3DE and ASWF projects since they're a key part of our tech stack.
* EXPO PAsses $20, will be putting more information and coordinate with Naomi and Crystal.
* We fell a little short of what we wanted to do, but we wanted to aim high, and we have the 
  booth opening.  Once we get connected with red hat gaming distro people, other people who are involved
  in the fringe and make a stronger bridge between devops, media, and DCC its going to get bigger and
  bigger.
* At least we got a booth! Come hang out at Linux Scale at the booth.  I'll have snacks and drinks and 
  candy for booth visitors.
* So cal blender group / MPS demo game, virtual production is being shown, several ASWF libraries, showcasing
  blender, krita, other opensource apps.

### Announcement JT - Check the news on Chinese MMO Gaming
* Seems as though other propreitary game engine stock has slid a little bit.  It doesn't mean anything
  but there are a lot of development in the news, in the global gaming mmos, China and other countries, you
  may want to check that news.

### Discussion - we discussed https://github.com/o3de/o3de/discussions/19539
* Sid:  try to get CPU bound / GPU bound memory, etc.
* Get the CPU Ms/Frame from IMGUI gpu profiler/ CPU profiler.
* You want content that is heavily CPU bottlenecked on memory, outside of that these numbers can be noise.
* https://github.com/o3de/o3de/pull/19332
* (Arbiter) Lots of small allocations across threads, where multithreaded tools it shines there.  Runtime
  perf was similar.
* colinb: This provides consistent usage across all platforms, and you can write your own.

### Discussion Topic - PopcornFx + WWISE
* Should we strip the PFX / WWISE OUT?
* colinb: I think its a mistake to put 3rd party stuff in there.
* JT:  We should see if we can tag the last known good version that has the PopcornFX stuff in there
* JT:  there's songs in there, helmets, skins, they were in such a rush to get it finished they scaled down
  but there's a ton of work in there.
* JT:  Sandbox you can further develop oen 3d engine features.
