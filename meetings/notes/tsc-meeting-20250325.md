# TSC Meeting - 03/25/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L.A.
* Jan Hanca [Robotec.Ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* LinuxFriend
* lsemp3d
* Matteo [Loherangrin]
* Mike S. [Carbonated]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Jan Hanca [Robotec.Ai]
* https://github.com/o3de/sig-simulation/pull/96
* https://github.com/o3de/sig-simulation/pull/95
* https://github.com/o3de/sig-simulation/pull/94
* One involved splitting extras

### Announcement - Joe Bryant [O3DF]
* I was at scale and GDC
* JT was with me for the scale event. 
* I met with several people and posted a list of things to talk about particularly from GDC that had the most
  questions and feedback.
* Scale was mostly introducing people to O3DE
* We don't need to talk to all 9 points since people in TSC have been answering the questions already.
* Mythica Package Browser open source tooling.  I was wandering the indie hall.
  * They said "Hey, we know you're looking for a pacakging solution for allowing people to easily find packages you have."
  * They showed me a thing which displays packages (gems for an exmaple) and actually shows an organized list, it has the ability
  to display graphics, animations, other pieces of information about it, they are open source ing the entire solution.  
  * I was looking it, its perfect for what we need, it reformats for PC, Mobile, Mac, for displaying our library of gems / whatever,
  here's info about them, etc. 
  * I'm not saying we have to use it
  * We should take reviewing it seriously to see if its what we want?  Can they send screenshots, etc in action, URL for the github
    that the code is on.  Which SIG takes a look at it, and which SIG takes it on for reviewing the code and tool itself.
* SIG Content and maybe SIG Core?  Maybe its a workgroup thing.

* There's also a financial services company, trying to stay way under the radar (FINSvc is cutthroat).  They are implementing some
  really cool features for O3DE and want to wait until they are further along in implementation.  With Your leave, Nick, I'll talk to
  some of the involved in Sig-Content like we have for some other companies so that they can talk freely w/o their company talking
  on full discord.  WE DO NOT SIGN NDAS but they'd at least be happy with such a channel.

* I had a random invite at GDC, a company called  Two Giants entertainment is using large pieces of O3DE (atom, O3DE Core) then they
  have their own custom tooling around that.  They are made of individuals working at other companies like ubisoft, etc.  They have
  nothing but complimentary things for saying.  They are asking about v20 for c++ standard.  They asked about what our future plans were,
  I've encouraged them to start discussing on discord.  
* It means they can help 'sell' o3de tech internally to other companies that they work with.
* There are parts that are poorly comments, particularly in the core in the engine.  Overuse of templates, some of the esoteric c++ 
  feature usage, we've had discussions to try to lower the use of templates, it raises the bar on contributing back.  There are areas in the
  code where, good luck trying to contribute to.  Decomplicating the code is going to take some time.
* Try to avoid in the future, when reviewing the code is esoteric c++ features that 1/500 engineers will know anything about.  We are
  and open source project, live and die by our contributors, but we need to make it possible for contributors to contribute.
* Having managed dev teams for 20 years, "Its great that we have these smart people that do this stuff but we have to be able to hire
  new people to maintain and contribute rather than the bar being so high that like 1/500 engineers can contribute."
* Sig-Core should create a RFC to tackle this long term.
* It also increases our build times quite a bit... templates were #1 on the list.
* Steve P [Amazon]
* JT (DOCS) will be working on this in the docs.  I actually worked thru several projects with this exact issue.  You have to put key
  statements about things that people struggle with.

* I met with popcornFX. They had a booth! 
* They had the O3DE Logo in their booth, awesome.
* They want to work on a hardware acceleration in O3DE, they want to get it in for O3DE.  Fortunately Sig-graphics-audio has already talked
  solutions and I'll get that to (POPCORNFX).  I'll have them join the channel or play go between.  They are committed to O3DE.  

* PS5 support.  I cannot talk publically.  We are persuing it, we are going 3rd party.  The foundation cannot sign agreements that Sony is
  going to want.  It has to be done 3rd Party.  Really, Ps5 supports all we need - we have XBOX, Nintendo.  The person who is helping out
  is on a plane, cannot chime in.  Mostly, we are persuing, its taking longer with sony - it took godot several years for example with sony.

* Game Telemetry - I talked to companies (3rd party provides telemetry).  The foundation can provide hooks in the engine, to support
  telemetry, but we cannot actually store the data.  The reason for this is as an open source non profit foundation, basically it would
  be having peoples gameplay data on an open server, etc.  GDPR, etc.  We try to touch this as little as possible.
* I've talked to some 3rd Parties (DataBrick being the most viable option at this point) and what they're going to do is work with their
  partners, and then they're going to look at creating a gem for that.  But just know that the foundation will not have an option for
  storing data (in the foundation).  Game telemetry is extremely important for figuring out whats working and not working, etc, but
  we cannot store data (in the foundation).

* Crash reporting and profiling.  It was pretty common.  I want to see if someone wants to give a talk on profiling and crash reporting
  in o3de for the next connect meeting.  Guilliame? (They are  not present)  
* Sid: I pinged that thread.
* Sid: He added support for tracy and superliminal, and optick profilers as integrations by gems.
* https://github.com/o3de/o3de-extras/pull/834

* GDC had 12 meetings planned, and equal amount almost unplanned.  NOt just socializing, most of it was spent talking with people about
  O3DE.  People using it who we had no idea about.
* Reiterate:  Its this community that makes the wheel turn.  Very appreciative of that.  Allows us to have successful GDCs.
* There were no Game Engines with a booth at GDC.
* Sid: Were you able to connect with virtuos?
* Joe: One of the engieneers for virtual geom tech was giving a talk.  But I kept missing them, they were always busy doing something
  else.  Their tech people are usually in meetings and talks, with their PR people dealing with booths.
* A lot of booths were doing interviews at GDC and trying to hire.
* Same thing at Tencent booth - they were trying ot hire, and didn't have much in the way of Business Dev people.  hiring was common!
* Lots of recent graduates looking for jobs at GDC.
* JT: Did anyone mention one specific gaping feature (We would use you but you dont have this feature?)  
* Joe:  Conversion from unity.   Unity had almost no advertising presence in any of the booths.  If you didn't know about unity, 
  you would not have known it even existed at GDC.  Lots of people looking to move from unity to something else.
* Company is working on it, getting it easier to convert to O3DE.  They ahve already made a ton of progress, monobehavior up and running
  in o3de, but, I'm a little scared of that, not sure its something we want in the engine.  C# for example might be useful.

### Discussion
* Nick L - levels caching data.
* lsemp3d - I didn't dive too deeply into this, I'll read it again.
* (Discussion about script events)

