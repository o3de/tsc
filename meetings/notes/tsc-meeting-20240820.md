# TSC Meeting - 08/20/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Nick_L
* Jan Hanca [Robotec.ai]
* Lloyd T. [Carbonated]
* null [meta]
* Steve P [Amazon]
* Sid_Moudgil [Amzn]

## Agenda items
Agenda Topic: https://github.com/o3de/tsc/issues/137

## Announcements
none

## Topics from Agenda
none 

## Open Discussion
* Installer is not working - Steve to get ahold of Mike

### Sid_Moudgil:
* Mike responded about AZSLC, we need an x86 version of it.
* He created a PR for it.  He hasn't kicked off the github action.
* Need another PR after this.
* Akio finished the last big optimization that will extremely beneficial for android
* Its in the development branch, its up on PR, we will have to find some time to go thru it slowly
* We're expecting 20-25% improvement.  It reduces your memory movement by a lot.
* Whenever you merge 2 passes together, you are reducing all the render target memory that needs to be moved out and back.  Do that across 3-4-5 passes you have reduced a lot of memory movement, it has a significant impact on everything.
* We've been working thru all the problems on that PR.  A lot of that work has been inspired by a the work that Galib has done on the VR.  Akio took it and made it fully dynamic and brought it to the mobile pipeline.  It should help across all mobile and VR. 
* Its only on vulkan right now, asking them to look at Metal.  It still needs a metal RHI support for sub-passes.  that will take some time.
* Pixel 8 is 1 year old.   Its vsync bound.  He went from 80 fps to 110 on shader ball scene.
* early january last year, it was running at 15fps.  From that to 100.

* One problem we found was that the mesh feature processor was building draw packets in the simulation tick.  If you change the render pipeline in any way that can cause some problems in backends like vulkan because your render config hasn't been established.  Your passes config could change int he same frame and complains.
* Especially when you change pipelines, people can for example disable depth of field or something and you get 1 frame of badness. We may well have to look into once the sub-pass stuff is fully done.  It will impact... we're changing the way the frame structure is set up.  Its going to be pre-update tick, which updates all the pipelines, then simulation tick, then render tick.  Handwavy but without decoupling it in a much larger comprehensive way, this is the best solution for the moment that we think makes sense.


