tsc-meeting-20231107.md

# TSC Meeting - 11/07/2023 

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]


## Attendees
* Nick_L 
* geds-dm [Amazon]
* RoddieKieley [Red Hat]
* colinb[apmg]
* Nana Yellen
* geds-dm [Amazon]
* sid_Moudgil [amazon]
* null
* Naomiwash
* Joe Bryant [amazon]
* steve p [amazon]
* sanb [amazon]
* Luis Sempe  [Amazon]

## Agenda
(nick L was out on vacation, no agenda was posted)

Ad-hoc Agenda Item:   Nick L will not be around next meeting

## Discussion
* geds-dm - release build application - do we want to support them in release build configurations
* Joe Bryant - leaning towards the profile tooling in there, with the release build stuff too.
 - lot of work has been done to get the editor and asset processor to work in release, and the main
   reason to do that is to reduce the size of the installer, but the risk and the amount of work needed
   and the risk that we will miss something, for the point release, I'm okay with making the installer
   a bit larger but safer.  We should discuss this for the next major release, a longer conversation
* geds-dm - release is meant for final release to my customer.  monolithic release was meant for that,
  but we have a couple configurations that are almost never used.  Rarely use monolithic release.

The main concern is size of the installer.
Current installer has monolithic + non-monolithic 

* monolithic release is non negotiable since its the smallest possible release you can make.
  * it should be called 'final shipping' rather than release?
* profile is for building tools and working as a dev team.
  * its like debug with optimizations.
* proposal - installer can selectively add other configurations.
* the numbers - if we include release non-monolitic sdk + monolitic sdk 9 gigs uncompressed to 5g
* not seeing red flags for size.  
* Decision - point release will ship with profile (so editor and tools run) and include monolithic release sdk
* Decision - 2024 investigate for next major release - getting editor and tooling for release.  How to make a release build and what that will take... being able to dynamically download what you want.
* GUI/UX stuff will come for the next major release, likely (maybe february)

## Naomiwash - topic - O3DE Connect
* any topics for the o3de connect?
* Its going to be a QA otherwise.
* Talk about the point release.
* Warehouse demo from roscon.





