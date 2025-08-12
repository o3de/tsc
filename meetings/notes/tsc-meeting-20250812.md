# TSC Meeting - 8/12/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L. A.
* colinb[APMG]
* Jan Hanca [Robotec.ai]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* Tobias Alexander Franke [Huawei]

## Meeting Notes 

### Announcement

### Discussion - Release Versioning Strategy
* https://github.com/o3de/sig-release/pull/354/files?short_path=266993c#diff-266993c75289497846fa885c55a2cc1755c7e6b7c0139c0fa326a04c9831de08

### SIGGRAPH USD Working Group Collective Project 001 - JT [SCB_GameDesign]
* ODIE is being used in aUSD file in a workflow and went realy well.  I'll let joe update everyone when he gets back, but it went
  really, really well.   We'll coordinate on socials about it.  It was well attended and quite a few people from the game and film
  industry.

### Discussion - Colinb - Schema 2.0
* An area where we have to do mappings back and forth between platform naming conventions, cmake has their own naming platform convention,
  we align pretty well between the two.  But we diverge on the open platform for mac.  
* We use "MacOS" and that's used throughout the engine, platform folder for example, you'd see "MacOS", but CMake uses "darwin" for such
  things.  I was just wondering if anyone cared about that.  We were thinking of doing more work on mac and if we became closer, would it
  matter to anyone?
* Sid_Moudgil : didn't we have that and then revert it.    There was a reason why, we had darwin, and we switched to mac.   Is there a 
  reason we switch back?  Lumberyard used darwin, but we moved to MacOS.
* Sid:  It is differnet but its changing now that macs are essentially a big tablet going forward.
* Mac, mac, MacOS, apple, darwin, inconsistent at the engine level, if you go into the engine's cmake platform, its "Mac", elsewhere its 
  platform_macos.
* Mac means intel mac, apple mac.  Mac has everything will run on intel mac, apple mac, editor.
* "Mac" is the offical platform name and platform wart is "mac" - iOS for name small wart.
* In the future we want to get rid of intel mac, in its current form, right now, it doesn't work, you need a bunch of DXC thats checked in
  its built from a M1 computer, we don't have a pipeline for DXC, to run it on intel you have to rebuild that 3p package and check that in
  and use that.  So going forward, intels will be deprecated
* Steve:  If you build on a apple silicon mac, it builds apple silicon binaries.
* Sid: Even the render pipeline that mac uses, its tile gpus under the hood, the PC render pipeline doesn't apply to mac as is, it is mobile
  hardware, so you'd want to build a mobile specific render pipeline.
* Sid: Replace the mac scripts with the arm64 scripts in the release after this work goes in.

CONSENSUS:  
* "Mac" is the capitalized to use for the Apple laptops, Mac Minis, Mac Pros, etc for official naming in config files, folder names...
* mac lowercase is reserved for filename warts like platform_mac
* Mac refers in O3DE to Apple Silicon chips, and going forward, we will not support intel chips which are being deprecated since the
   introduction of Apple Silicon M chips 5+ years ago.

### Discussion - colinb - Schema 2.0 restructure restricted objects
* The way the Platform Abstraction Layer, the open engine o3de, has support for mac, windows, stuff like that, in the platform folder 
  there's the name of the platform and we wart the files.  When we do cmake configure, we go across the platforms, it will try to load
  those platforms in a way that CMake understands, and based on your configure command line you can specify a restricted platform to
  be built.  So if its a platform NOT inside the open platform like a console or a secret platform not released yet.
* For example there is a PS5, there is no PS5 platform name or anything like that, and even if there was one, we cannot release it,
  its restricted, its not open code, we can't put it in the open engine.
* The way we get around this, is via restricted object.  Its an object that extends an open object.
* The engine itself has a restricted engine object.  Inside that object is a folder sturcture that mimics the engine's folder structure,
  and up to the platform level, so for example, cmake/platform/ new folder that was for a certain platform.  So for example, PS5,
  cmake/platform/PS5 folder.  This way, when configure runs, and you specify "I want to build for PS5", it goes to the open engine, 
  and looks for cmake/platform/PS5 and finds its not there, and then says, ok, engine object do you have any restricted objects,
  I happen to have one, here it is, it goes looking in that folder, cmake/platform/PS5, it uses that file instead of the one that
  would be in the open engine.  we can do this throughout the entire object to add a platform to the engine.
* The way the restricted currently work, any object can have at most 1 restricted file.  This was a hold over from the lumberyard days
  since o3de, and it was all in use by amazon at the time, it had a very specific use.  In that case, we simply put all of the
  restricted platforms in one file, that restricted file, because at most, the engine could only have 1 restricted objects.  We had
  no combunction, we had all 3 licenses for hte platforms that were supporting.  PS, XBOX, nintendo.  We could put all 3 of those
  platforms in the same restricted object, and it was fine.  Everything would work.
* However, that is no longer hte case, we're not amazon or anything and customers have different licensing, so carbonated, others, 
  APMG, they have 1 license for example, they are not able to see the other platforms, so restricted objects can not be given out
  to people, they ahve to be hand edited and certain platforms removed and certain platforms remains, its very manual and inconsistent.
  It wasn't planned for scale.
* I'd like to make it so any object can have multiple restricted objects and they can have multiple restricted objets in them if they
  wish.
* So for example one for PS5, one for XBOX, one for Nintendo X, they could be in one object, but the more importantly, it could have
  multiple objects.
* The current workaround is that you do indeed have different objects, I want to switch, I would have to go into the manifest, and
  disconnect all the restricted objects, and reconnect and reconfigure.

### Discussion - Schema 2.0 is contemplating a new object type and its called Overlay
* Its very much in the vein of restricted, but its not restricted.
* Code is immutable, or, I'm using something and I want to make an overlay object has the same structure as its overlaying but when
  cmake runs, it consults the overlays and precidence.
* If I was going to overlay the engine object, I'd link into that tree from the engine object.  The process would take care of 
  all of the things for you.  The directory sturcture would look normal to you, but all the files would be there.  Any time you
  link to a file you add it to the gitignore of the overlaied file.
* Other way would be to build a tree of links from the source objects, the build itself would take place out of a different folder
  to the object itself, no mixing of git trees, git ignores.
* Reversed platform structure inside the restricted, platform comes firest, and is removed from the path.

