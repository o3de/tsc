# TSC Meeting - 5/27/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Luis
* Matteo [Loherangrin]
* Nick_L
* Reece H. [DrogonMar]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Joe - Welcome Hellaenergy (Nick) [Red Hat]
* HellaEnergy is our sig-chair for sig-release.  He will be taking over.
* It is a slow transition so he isn't thrown into the deep end of the pool instantantly.
* Hellaenergy: thank you for having me and I look forward to the challenge.
* Joe: Where are you from?  
* Hellaenergy: Minneapolis, USA!  There's roadwork on my street.
* Joe: We have people who join who have rolling blackouts.
* Joe: I'm still managing this release, nick is still learning about the release.  Once we're through
  this release, nick will take everything over.
* Nick: Point release is easier learning
* Joe: speaking of the release, we are on track for releasing next week.  Release dry run is posted, is everything ok
  for the release.  Marketing is also prepared for the release.  We are advertising the webinar for the following week (11th)
* Nick: HDR stuff?
* Reece H.: Current state of that PR it doesn't check for colorspace.  Its possible you'll get a 10 bit image, and not 
  correctly check the color space, so it will call a function and resulting a validation error and will crash.
* On windows, if you have HDR enabled.  
* Joe:  Whats the previous behavior?
* Reece: It would just use SDR.  Would be a normal HDR?
* Reece H: the other problem is that it didn't add another vulkan extension, you need 2 vulkan extensions loaded to have it
  correctly work.
* Joe:  There was no hdr behavior beforehand, so I will release note it.
* Joe:  If you have HDR eneabled, while using editor, you may experience a crash, weplan to fix it in next point release.
* Sid_Moudgil: You just install the engine, crash.
* JOe:   Request reece today get that review in and get 7 days to day.
* (Discussion, we are going to try to fix it for release, TODAY)
* Reece H.: Anyone who wants to expand the HDR functionalities of this engine it should be pretty easy to expand it to the RHI
  for DX12.
* Reece: I wanted to bring linux on par to the windows one.
* Joe: Note I will be travelling june 9th - 14th, then 19th - 23rd.  I'll be messaging people who live around that are or are 
  if you're around or attending AWE in long beach.  I'll try to put together a contributor lunch.  I'll post in general chat.
* Going to open source summit (LF event).  End of june.

### Discussion - Sid - Graphics
* New implementation for motion blur - it is now approved, it is same implementation as call of duty game from 2016, so its
  pretty good.
* Big push from huawei to redo the material system, he is aware (karl) that this is a huge refactor.  
* Material system is duplicated across all our pipeline and the raytracing shaders.  
* Its going to use bindless, and centralized.  All the traytracing code and pixel/vertex/rasterizer code should point
  at the same material SRGs that is centralized.  So if you have bindless support it will have 1 material SRG, if you
  dont', it will create a SRG per object.
* Its a huge refactor.  Once it goes in, it may inpact people shaders, anytime it goes materialsrg, most of it is
  already done, its only if you have your own pipeline.  Very few people, its a small change.
* There are more changes that are coming down the line.
* Joe: The impactful change is already in.  
* Sid: Meta has been doing extensive testing, we've been doing extensive testing, it runs on pc, linux, meta runs it on
  vr/ar mobile, the next step is to merge.
* Joe: It will likely bein the october release.
* Joe: There's the raytracing one, I'll post it in the release notes.
* Sid: There's a whole bunches from huawei which is related to multi-gpu.  
* Joe: Later today I'll do a rough count of bugfixes and fill in that number.
* Sid: I tried to capture that in our release notes, there's a long list, but, I don't know if I captured everything.
* Joe: There are SO MANY bugfixes, it would be like a dictionary.  What I do is in the summary paragraph, I just put
  'we resolved x bugs' however many it is, and its up to each sig to choose which bugs bubbled to the top .  Its an
  impossible task to be honest.
* JT: Q for sid: We stated exactly what changed.  Is there a document on what to do with the changes that are made
  in the material system?  Not just what has been done?
* Joe: Yes, it says exactly what you need to do, with code snippets.

### Discussion - Sig-Core - Steve P
* I posted an RFC - we're converting the framework libraries to shared libraries
* REduction of binary sizes, initial findings based on WIP branch, 50% at least saving.
* On linux, I was seeing 70% binary size reduction, showing you how much the static libraries were taking up.
* Debugging in linux was impossible it would eat up all your memory, every single shared library would load its own
  debug symbols which were copies of azcore, azframework.  the RFC is up there, my plan going forward is to make this
  branch that has all these changes in a public branch for a while, testing it, fixing it.
* The only issue I have so far, being able to load a project, building multiplayersample, it did run except for some
  Popcorn FX assets not laoding
* There's some issues with leaking RTTI libraries, some of the unit tests, some fail due to DLL allocation errors.
  That should be going up pretty soon.
* I'm going to build the installer with these changes, going to see how big the final debian packages will be.
* Sid: currently we had to some weird workaround for CVAR you had to use a special API - does that still work? The
  workarounds we had done should still function.
* Steve: Since the CVARS do have actual storage, this should alleviate all the cvars.  This will only affect cvar
  that will be declared shared libraries.  Those will be available across any module or other boundary.  If you
  declare a cvar inside a gem, it would work the same way before.  None of the gems are affected by this, we are
  not changing the gems themselves, only the core shared libraries.
* Steve: I'm going to have to add docs on how to dev on core libraries.  Public branch instead of a PR is because
  it affects 1500 files, nobody is going to reveiw a 1500 file PR.  It will be available for view, but its better
  that people can use the branch for now, and once everything feels as stable on dev, we can merge to dev.
* colinb: I'll be doing the same thing for schema2.0 changes.
* Steve: I replayed all these changes, each individual commit has a title, has a small subset of files.  If you
  look into the history of that branch you can see the diffs.  One of them you can see "AZ_API macro" and another
  would be like "Introduced a new CVAR".

### Luis: Sig-Content
* Standard working issues, recent files on the asset editor, quality of life.
* Thats primarily the focus on that side.
* Guillaume: i'm looking at the sig-content proper labels to see how many editor crashes we have, how stable
  are the tools, etc.  We went from 30 pages down to 12.  Done by end of week.

### nick: sig-build
* AR / Github AR
* Joe: We're looking into a fully offline installer.  Behind state or univeristy firewalls, that block downloads
  of things like python, so I talked with mike about it, once we get GHA issues resolved, we'll look into this
  fully offline installer.  Its mostly offline but it does 3 major tools to download after its finished download
  and installed and thats the ones that fail / break the installer and it can't download those files.
* Joe: The installer should not be doing those post download steps.  We'll do a fully offline installer for now.
* Joe: Why we're moving to GHA for our current pipeline, its because right now anytime runs AR using our curent
  pipeline it costs the foundation a lot of money.  GHA is free but slower, we can run it as much as we want and
  it won't cost anything.
* There's 2 people from CnCF that can look at our build pipeline and see any optimize foundations.  Thats a huge
  open source project.  you're specialists, can you take a look at our package and build?
* colinb:  MS is a member?
* Joe: Many members before I became the Executive director, there were weird AWS deals, can't go into the details
  but theres a dropoff.  MS is not one.  Some companies lost faith that it would be run, and I'm working on 
  getting those people back.  MS was for 2 years, is not currently.  Its funny because I talked to microsoft
  and I'm talking to get azure into o3de so that we'll have AWS and AZURE and then get google and maybe get them
  in and talk to the gaming teams again about joining the foundation.
* colinb: We can possibly get github runners on trusted hardware from members?
* Joe:  We have to do that anyway.
* colinb: Dedicated hardware that they're willing to devote to the project could speed up AR times.
* Joe: JT needs peopel to contribute to mac, but we can't until we get some way of running AR on mac.
* JT: I have another person whos wiling to build and setup mac.  I have time this week and gather information
  and I've talked to steve and sid, we have enough of a critical mass to work on mac building for all aspects
  of mac for this next release in october.  Total of 7 people who are willing to work on people.
* Joe:  Bandwidth costs for hosting that machine.
* JT: Tehre are servers that give 100 buck credits for running this, I'll check in with AWSF and check for that
  100 credit.  
* Sid: We need native arm64 support.
* colinb: Sig-platform topic, steve has been having a success porting to arm on android.  
* joe: We have ARM server support.  We can follow the same roadmap.  We can follow it for ARM silicon.


