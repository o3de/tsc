# TSC Meeting - 09/10/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* akioCL
* colinb[APMG]
* Jan Hanca [Robotec.Ai]
* Joe Bryant [O3DF]
* Michał Pełka [Robotec.AI]
* Naomi Washington [LF]
* Nick_L
* null [meta]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* Tobias Alexander Franke [Huawei]

## Agenda items
Agenda Topic: https://github.com/o3de/tsc/issues/140
* Sid_Moudgil [Amzn] - WebGPU

## Announcements

### Announcements - Joe
* Joe will be out from fri 13th to the 23rd, back on 24th.
* I'll be able to respond to emergencies but thats about it.
* If you want to see the new mascot, attend tomorrow's connect meeting.

## Topics from Agenda

## Agenda topic: Joe Bryant [O3DF]
* Tomorrow during connect I will be going into more depth on the release.
* Just so everyone's aware, we are soon going into all code freeze.  Monday 23rd is code freeze.
* No code will be allowed into stabilization without prior authorization from sig-release (Myself or Roddie).  
* I will link the dashboard in discord and figure out how to get it permanently displayed
* We do that to protect stabilization
* We are making sure we are not inadvertently creating more instability in the release, even for bugfixes, which can cause instability.
* SIG-release meetings will be used as planning for the release, so there's one today.  Every 2 weeks after.  The most important one will be on the 24th, that is the assigning roles and making people aware of what they are responsible for the release.  
* Joe:  nick, Are you interested in doing the integration to main?
* Nick:  I will do it.
* Joe: Wednesday Oct 9th is release.

### Agenda Topic: webGPU - Sid_Moudgil [Amzn]
* We are getting a head start on WebGPU.  
* O3DE running on the web is a huge effort.  I want to make sure that this is happening and what the high level strategy is.
* There is no RFC but we kind of know what to do for this, we will make an RFC if necessary for the bigger effort.
* What we do need is a bunch of things:  We start with the WebGPU RHI.  The way we plan on implementing that.  We use a google library to make it testable on PC and chrome.  The idea is safari, mozilla, etc have their own impl, they are all in different beta/preview stages.  For now, we'll use google Dawn and test on PC, but in theory it will eventually work on all.  we're nowhere near yet.
* Akio is spending time in the RHI, and already has a triangle rendering in Dawn.  There are going to be a whole bunch of restrictions in the RHI.  A lot of them are GPU API Driver restrictions, like "only 4 shader resource groups" or "only 10 buffers" or "16 textures" or "no array of buffers", etc.   Lots of restrictions we are going to have to work around.  Some make sense, some don't, like, the gpu should not have those restrictions.
* The RHI is well understood, the RFC is not needed, we already have 3 RHI backends, this is the 4th one.  The next stage would be to build a render pipeline for webGPU. A ll of these restrictions would mean you have to enable/disable a whole bunch of stuff and make sure its performance.  Then the engine can open up for non-rendering changes.   And we'll need help there - we're confident about rendering, but after that, the non rendering stuff is a bit of an open territory, what needs to be done there is that we're hoping we can get contributions from other companies there.
* We need to convert the whole engine to webassembly.  It is a huge thing, theoretically not - but it could be a huge thing.  We don't know what kind of issues you could run into.  There could be 3p library problems.
* Step 1: The current engine is quite large, 200mb for example, maybe 500mb, but its fairly large, we need an executable disk size at least in the hundred meg vicinity maybe less.  Unity is around there, I think.  Not sure.
* Cut out every 3p package, every gem that isn't contributing to web rendering or whatever level you're running.  An o3de-lite kind of thing.  After that you'll have to add the editor workflow that spits out a webjs or html that can run in the browser.  You can then use dawn in chrome you can have a version running thats further down the line / next year if people contribute to this space.  
* Further down the line we want to add webxr, should be fairly easy if webgpu already works.  In theory you could just put on a quest 2 go to the website with quest2, webxr support is being discussed by webgpu folks.  You could distribute XR content via a website.  downloading a big runtime etc is a big barrier to customer experience.
* Sid: Akio, could you speak about it?
* Joe: Sid, could you and AkioCL talk to Royal about WebGPU?  They are planning to use O3DE for the project.  If you can reach out to him on discord and schedule a discussion with you and AkioCL, we should be trying to join forces with his resources if you can, it might help it go faster implementation-wise. 
* Akio: I've been working on webGPU.  The impl is pretty straightforward because webGPU is like our RHI.  Mapping it is pretty easy, so the impl is going pretty fast.  I've already got textures, meshes, shaders, all of that is running.  The big issue is the limitations of the webGPU itself, the resources is pretty limited in webGPU.  # of textures, # of buffers, teh # of srgs, is limited, and its limited in Dawn (the library that us and chrome uses), its limited by Dawn itself, not hardware limited or webgpu itself.  I don't think its going to change so we are going to have to adjust o3de.  Similar to a mobile pipeline, is what we're going to get on WebGPU.  
* Akio: The implementation is going forward, we're doing good.
* Colinb: this dovetails a little in the effort to remove the core gems into an extras repo.
* Colinb: lite version of the engine to use for other applications.
* null: Making a small change to aznetworking that would allow me to plug in webRTC, another open source data channel we can ask for unreliable (ordered/unordered) and run the multiplayer system over webrtc and would work well.  It would give engine access to voip and potentially web cam streams.
* akioCL: I don't know why they limited it so much.  I want to make it run on every user.  but what if you want to make a high tier application but you are limited by these numbers?
* akioCL: probably the least common denominator.  I looked at the other implementations and they all have similar.
* Sid: I was thinking as webgpu usage increases, I think they will revisit and up the numbers or whatever
* AkioCL: a lot of things they apush for a future version.  They are pushing hard for a 1.0 version, and a lot is pushed for later, and they primarily want a release that works in all browsers, etc, and will push for a more complex version later.
* Sid:  just to resync, once the RHI goes in, it opens up the core conversation - the hard part is here is conversion to webassembly and optimizing the engine for size.  Thats where the next big effort would need to be done. I 'll reach out to royal to see if he has capacity in this space.

## Open Discussion
* no topics

### Discussion: no topics

Remember, the mascot reveal is tomorrow during open3d connect (8am PST) see event in discord.
