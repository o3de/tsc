# TSC Meeting - 3/7/2023

# Chair and Co-Chair
* nick_l[amazon] 
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L [Amazon]
* Tobias Alexander Franke [Huawei]
* RoddieKieley [Red Hat]#4265
* geds-dm [Amazon]#8414
* kberg [Amazon]
* colinb[APMG]#6994

## Agenda Items
https://github.com/o3de/tsc/issues/71

1. Discuss minimum version of windows required (for raytracing shader stuff)
2. Mobile Working Group update

### Minversion of windows
* The following is a summary of the discussion that occurred.  There were many opinions and considerations in a very short time.
* TSC and present members disagree that windows 11 minimum is okay, it would cut ~70% of the market out currently.
  * Windows 10 is still largely in use (from the stats)
* We'd like to know how many people who are below 20H2
* (The TSC did some research and found a market share graph - 20H2 is the ideal.)
* Summary of the TSC guidance:
   * Use 20H2 as the min version until something forces us to 21H2
   * Make sure that any installation requirements are taken care of - either automatically, or very carefully (work with sig-build and 
     sig-release!)
* https://github.com/o3de/o3de/pull/12009 has the same graphs and data.

### Mobile Working group update  (by Tobias)
* First meeting in the voice chat
* Mobile working group repository on github
* Two items that were posted on github
  * Would be nice to have a mobile label to mark issues that are also mobile issues
  * Once we've sent out the invitation to figure out a fixed regular meeting date, I'd like to add a calendar entry into the official O3DE calendar for the working group mobile.
* 2 people from the community and myself (oppo, etc)
  * First was to establish what everyone was working on
  * Major discussion - whether we should do glsl - various things to organize the roadmap.
  * I'll post the notes soon in the repo.
  * https://github.com/o3de/wg-mobile


#### Mobile Label
* tobias: it would be an easier to find them more quickly and assign stuff to people or to put them on a roadmap of sorts.
* already have a roadmap board (turn it public)
* Label:  wg/mobile

#### Mobile Email list and calendar
* nobody had problems with adding email list and calendar.

