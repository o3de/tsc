# TSC Meeting - 12/12/2023 

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* nick_l
* geds-dm [Amazon]
* Joe Bryant [Amazon]
* Naomiwash
* RoddieKeiley [Red Hat]
* Steve P [Amazon]
* Sid_Moudgil [Amzn]
* Luis Sempe [Amazon]
* Sid_Moudgil [Amzn]
* Danillo [Amazon]
* Sergio Rojas
* Michael Pelka (Intermittent)

## Agenda items

### This meeting is recorded.  
You can listen to the exact words yourself at 
https://drive.google.com/file/d/1NhNPinA90ooEG343BbVt26rPKw1bXlHy/view?usp=sharing

### Ad-hoc Agenda: (Joe bryant - Physx gem will be two gems, but one source code base)
* Small discussion on the plans for the physx gems - they will

### Ad-hoc Agenda: (Joe Bryant - timing for next release)
* Joe:  Next release - GDC is in march (18th or so), therefore I would like to suggest we time the next release for sometime at the end of february.
* Other reasons exist such as resourcing, but this would give us time to react to any issues (we usually have a point release before GDC hits) - and when GDC hits and we can point people to main instead of telling them to grab from branch or cherrypick PRs.
* Nick/Roddie: Four months worth of development.  What goes in to this release that diddn't end up in point?
  * Joe We'll have no-code project, 
  * we'll have project export UI, 
  * we'll have perf ops around asset browser, 
  * IOS and android support, 
  * ios and android packaging, 
  * physx 4 and 5 gem seperation PERHAPS (nice to have)'
  * atom memory optimization
* Joe: We're better off doing more frequent releases (less to test and you don't need as much of an army of people).
* Naomiwash: No reason to slow releases for the purposes of marketing.
* Joe:  Long term - supported releases (LTS).
* Naomiwash: Elaborate what a supported release is
* Joe:  Its a supported release where we specifically say we will support it for multiple years.  We will do bugs and fix updates.  
* RoddieKeiley: You have ot come up with a policy about what kind of bug, etc.
* Joe:  Foundation could charge support plans, etc.


### Discussion of roadmap / board (January 9th is 2024 roadmap)
* Goal is to have the roadmap agreed upon by tuesday Jan 9th.
* Joe: We have only a small set of resources to get things done.  If they want stuff added we will have to remove stuff
* naomiwash:  Boards main issue is visibilty and onboarding.
* naomiwash:  Anyone opposed to jan 9th finalization?
* Roddiekeiley: (Timeline)
* Joe:  Roadmap goes into June and is extremely high level.  I approach roadmapping historically by next quarter is detailed, next quarter has a good amount of detail but may drop off it.  following 2 quarters, generally high level aspiration, so much can change in 6 months.

### Ad-hoc Agenda: (Naomiwash) - should we cancel the all-sigs meeting?
* Yes, nobody will be here.  Naomiwash will cancel the meeeting and let everyone know.

### Ad-hoc Agenda: (Naomiwash) - This wednesday is the O3DE Public Meeting.
* Right now we have TJ Speak, and the Point release.  
* Joe:  I'll talk about the point release - it will be the day before it and I can talk about it.
* Naomiwash will post the meeting / slide.  We have project exporting and point release.
* Shader console will also be shown
* Naomi:  the more the better - last time it was AWS and LF mainly. 
* Clips from this were used as content generator, so it was very useful.

### Ad-hoc Agenda: (Naomiwash) - Annual report
* Other open source projects do an annual report - everything we've done in 2023.
* Do you all think this would be beneficial - plan to have this on the roadmap?
* Nick: Target Audience - LF would be the target audience and our member companies.
* Joe: I'm all for it - gives a chance to brag about all the things we've done for 2023.
* Will need help from Nick, Sid, Danillo.
* Naomi: We would not publish this until the top of February, but the visiblity would be good.  we are often asked what is O3DE doing.
* Joe: O3DE matured quite a bit in 2023.
* Naomi: I will get started.

### Ad-hoc Agenda: (Naomiwash) - Discussion of Mobile Working Group
* From Travis's note, it would be beneficial to keep it.
* TSC voted to get rid of it
* Joe: I convinced him that we should remove it, actually, and that we should move the contents to the platforms sig.  (It was never used, confusing for people, etc).  Therefore we shoudl move discussion into the platfrom group and have a sub-discussion group about mobile?
* Naomi: Let me know, its easy to do, and get rid of when we need to.

### Multi-GPU (Sid / Joe)
* Sid: RHI is in a good place for Multi-GPU support.  I've been trying to convince them to create an AtomSampleViewer sample for multi-GPU (for example rasterize one triangle on one gpu, one triangle on another, then show it in the main window).  They are currently trying to convert RPI.
* Sid:  they should prove out that the stuff that they are working on can work.  Please prove that out and test it out.  They are looking at it so that at least they can say we have multi-GPU in RHI.  But until we see some sort of rendering, we can't say we have anythign more than untested code.
* Joe: This is important because it will enable a larger customer set for O3DE.  
* Sid: It would allow people to render with multiple GPUs.  I don't think Huawei will actually check in a pipeline that uses it.  So there are many ways of doing multi-gpu, I think they will keep the Pipeline on their end.
* Joe:  The part Huawei is working on is a key pillar for anyone to build that pipeline.






