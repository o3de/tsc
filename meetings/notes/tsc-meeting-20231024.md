tsc-meeting-20231024.md

# TSC Meeting - 10/24/2023 

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L 
* geds-dm [Amazon]
* null
* colinb[APMG]
* nana yellen
* Naomiwash
* Nicole Huesman [LF]
* RoddieKieley [Red-Hat]
* SanB [Amazon]
* Joe Bryant [Amazon]
* Sid_Moudgil [Amzn]
* Sergio Rojas
* GI


## Agenda
https://github.com/o3de/tsc/issues/10

Agenda Item:   Nick L will not be around next meeting.

### ROSCon update - from Naomiwash
* Naomiwash - lots of interest in o3E from ROSCON - from robotec-ai
* Water element and drones came up.  Mike Balfour and Steve Pham, Sandeep there, consolidated notes.
* It was a huge success, so much energy around for O3DE.  We will send out notes to all the leads we picked up
* Resources and everything, we want to add a robotics page to the website in addtion to a game page, but providing them more resources
post-event would be needed.
* Joe:  "How soon do we begin amplifying?  Our booth, the presence there?"  Label any page we create Robotics & Simulation, not just robotics.
* Nicole:  We are starting today with the amplifying.  Robotec had a blog, and thats the first thing we will start with, and then if there are details
around (more details to put into a blog) I need a pointer to the demo, online, and we can amplify that.  We will start a steady drumbeat.
* Naomi: Need technical help on what to include, how to get involved, etc.  
* Joe:  Let me know if theres anything you need and timelines, I can work with Steve and Mike on getting info.
* Nicole:  We will have the social clips that we will begin running this week.
* SanB:  Agree about RosCon - One of the things I'd like to talk about is our differentiators, compared to other ROS2 capable engines.
  We are different to other engines, we scale more, can be more performant, single laptop with 36 robots was very impressive.  Talk about why we 
  want to use O3DE instead of other engines, including commercial ones like Unity and ISAAC-SIM.   Video is up on robotec but not the o3de site.
* Just need something written as to "why O3DE" why its not just another simulator, unique value proposition.
* Naomi will create a doc with the content we'd like to add to that, with everyones input as to what we want to include in that.
* ColinB - if theres assets or repos we can promote that might be a good idea.  
* Joe:  We have a couple of robotics demos that are available, I'll get the links to the repos for those.
* Naomi:  List of all the sensors we support.
* SanB - Do we have mention that we have importers for URDF and other formats, do we have migration instructions?  That may be worth adding.
* SanB - RoboTec met with Amazon VP (Bill Vass) and posted a public link on LinkedIn.
* SanB - OSSInsights - looking at the github stars . we went from 5 a day to 50+ a day with ROS event... 
* colinb - can we do our own video?
* SanB - People were amazed at the scale.
* Adam mentioned prefab overrides would be great to have in this release.

### Topic-Youtube
* Nana Yellen - our intention was to make something more professional, beginner friendly, similar to other channels.
* Basic tutorials are the best!

### Point release coming out on nov 7
* We need people to test it!  5 critical issues to resolve.
* Current status is on track to release on 7th.
* point release:  Turning on the prefab overrides, document property editor on by default, can turn them off.
* Material editor crash fixes, other misc crash fixes.
* Nicole:  Joe, what is your thought for the date in terms for promoting?
* Nicole:  We were waiting for a day or two after the relaese would go live, should we wait for the 13th or 14th to give the time to fix 
  things if they need it.  Joe is out Nov 10 - 26th.


### Ad-Hoc Discussion
* Consolidation of the Sigs.
* Naomiwash - were going to reach out to colinb - we wanted input.
* Roddie and Colin manage Sig-Core and SIG-platform.  
* Why not Content?  Content is a really large sig.  We talked about ops, doc-community, we're looking for sigs that were not active anymore.
* Docs are important to have a SIG as of itself.
* Also part of the conversions.  We are not going to merge docs - we need contributors.
* We're not archiving anything on the github.
* There is no rule that someone cannot be chair of two sigs.
* What about build and release consolidation.  Sig-release not to be merged with sig-build
* Lets think about Sig-Build and sig-release / sig-security  What about Security + Release?
* You need someone to hold security and release up at the same time.  Give Joe a couple days to think of it.  Will talk to Roddie about implications
  of security into release.
* Sig testing can be rolled into release.
* Sig ops can go away.
* Sig-network rolled into sig-core?  (No, pushback from many members.)
* Talking ourselves out of merging platform and core.
* wg-Mobile - transitory, for specific things.  Direct wg-mobile to the platform sig.

### Action Items
* geds-dm will run the All-Sigs meeting.
* Naomi will create a doc with the content we'd like to add to that, with everyones input as to what we want to include in that.
* Naomi will send out an email saying core has merged with platform, and we can choose which one absorbs the other.  CORE and PLATFORM
* Actually, we talked ourselves out of this due to the PAL.
* Naomi taking notes on wg-mobile.  
* New plan required for testing.  CTA did not work.

