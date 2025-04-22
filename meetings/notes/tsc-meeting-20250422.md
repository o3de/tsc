# TSC Meeting - 4/22/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Luis
* Matteo [Loherangrin]
* Naomi Washington [LF]
* Nick_l
* null [meta]
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Naomi Washington [LF]
* Release is coming up next month
* Last week I added quite a few calendar invites, one is today at 9:30 pt.

### Announcements - Joe Bryant [O3DF]
* Cesium has been given updated information
* Already started talking to people about what we need to do to update the plugin to the latest version of O3DE.
* Cesium is used a lot for digital twins, used for large scale simulation, example a city.
* I will continue reaching out and informing people of the progress.  I just sent it out on thursday and they said they received it on friday.
* We are in round 2.  We made it through round 1 at least for the grant.

### Announcement - Joe Bryant [O3DF]
* Deprecation discussion

### Discussion - Deprecation - Joe Bryant [O3DF]
* I need to send a flag to all the sigs - we need a deprecation plan
* Inevetably we need to do changes that break features and functionality.  Its just a part of growing and future proofing and adding/updating features
  for the engine.
* I have learned from history - you can not pull the rug out from your users.  If you want to lose users, break a feature that users rely on and they
  are done.  This is learned from experience.
* A Deprecation plan is a process for planning for a breaking change - informing users well in advance for a breaking change, and then having some sort
  of way users can use a flag to use the old feature, etc.  Essentially protects the users from rug pulls.
* A team halfway thru developing a game, lets say we break something around assets - it forces people to have to redo all the assets to work again
  with the new versions - that's an extreme pain point for users, and a lot of teams won't do it, its a lot of work.  It's a good way to just lose the
  trust of people and lose users in the process.  
* If everyone in this meeting is inclined, I'd like all the sigs to start discussing.
* Anytime you pull or change functionality for a core piece.
* In Sig-graphics-audio there is a change in materials, but, again, it could potentially pull the rug out from under users who were relying on that change...
* Sid_Moudgil [Amzn] - Its a full refactor of the material system.  The current setup in the engine is such that all the raytracing passes and so on had allt heir duplicated systems and they would duplicate the way material properties were handled.  They've refactored the material system, where hte same core logic builds all the materials and provides acess to them - any render passes - raytracing, rendering, compute, could use any of them.  It was previously a huge waste of CPU time and memory, its must needed effort.  Instead of e.g. 10,000 SRGS you just have 1 and have bindless to get access to the other ones.  Huge simplification of even CPU time because now you don't have to compile 10,000 srgs if you have 10,000 materials, you just have 1 SRG.
* The only thing they did as part of this change, given the scope of this change, they have to change the way you access Material SRG.  Now the API that gives you access, you have to go in the shader and change the way you access them.  It is somehting that is impacting every shader.  Every call in your forward pass shader is being modified.  They could give you a python script but even that is not going to be good - you don't know what people have done on their own projects.  There is no "all the shaders live in this folder, go in there, modify the API for them".  We discussed with META and Matteo and if they are the only 2 other people who have their own custom pipeline /modify their shaders, they will just go modify them.
* If you are working in dev over the next few weeks, this big change is coming in slowly over time, so the first one will drop soon.  Its been pretty much
  approved, needs to be tested by meta.
* Joe Bryant [O3DF] - The first step - post in the impactful changes change - that was followed.  A lot of people do not read the impactful changes channel.
  I suggest that in the release notes for every release, impactful changes for future releases.  We list the impactful changes we're aware of.  That's the communication piece.  One of the important parts of the deprecation plan is how you get the information out to users as efficiently as possible and ensure that your users read it.
* The next stap for the deprecation plan is "how can we make changes like this and  give users time to adjust for these changes and still do them."  Sigs are going to have to give us input on how to handle this.
*  In this particular case, becauase so few modify shaders, and because the people who do are very technical, add a section in the release notes - things to be aware of in future releases.  I'll list the upcoming deprecation/changes.  If we have a rough estimate of which release, I'll put that in.  Users do not like surprises.
* Early unity days they learned the hard ways.  Over time they've gotten really good at either auto updating peoples projects, or having flags that they would allow you to use the legacy system for N months.
* Sid_Moudgil - this will be for the october release.  Expecting the PRs to start going in, in may.
* Joe: Would be good to have an Impactful changes part of the documentation too.  Shauna, I can try to attend and we can do this.
* Sid: we can also check if meta finds that this really hard, we can ask if there's a better way to do it.
* Joe: I do read impactful changes as they come in, as the ED I'm not going to implement their deprecation plan - that's not my role, but as the ED, 
  I do help guide and have an over-arching view of the entire proejct and who are using it, I can advise and let people know what I'm seeing, and
  what kind of speed-bumps people are hitting.  But the sigs and community has to come up with what to do.  I'll give feedbakc and help guide bug I'm not the person who tells us how we have to do it.  Deprecation plans and then implementing them is a lot of work, its n't easy and its a lot of work, especially for large impactful changes.  What I want to do, this release is going to be pretty slammed for me, I'll set something up for after the release, probably very early june, if everybody's okay with that, I know that's pretty far out... but what do people think of having discussion then?

### Discussion - Issues for stabilization - Jan
* Are those issues there blocking the release. https://github.com/orgs/o3de/projects/68/views/5
* The short answer is by end of day to day we should have those triaged as well as for what absolutley needs to be fixed.
* Sid:  Please put a filter list for the sigs.  I'm trying to get meta and huawei a bit of time aside for this release... it would help to have that
  filter for sigs.
* Joe:  Formula I use for severity is impact to the user vs effort to resolve.  What the potential negative side effects could be if things go wrong.
  I'm happy to do that (severity analysis) but anything beyond that particular piece is going to be up to the sigs.   We don't have the technical
  expertise.

>Blocker: Highest priority. No workaround exists. Blocks users from using accepted workflows or crashes often.  
>Critical: Issue can be worked around but dramatically increases friction in workflows. Random crashes.  
>Major: Issue causes friction in accepted workflows, and can be worked around or avoided. Rare or difficult to reproduce crashes  
>Minor: Issue that causes minor friction or is a minor suggested change to a workflow. No crashes.  

### Discussion:  WGs
* Joe: I'm working with Naomi on the Working Group (WG) progress.
* Joe: Webinar about the release, about 2 weeks after it, we would like to have people talk about 4 topics about the release.
  Ideally short pieces (so 15 minutes or so for each sig talking) here are the new things in the release, maybe show some pieces of it.
* Sid: There's a lot there from graphics
* Joe:  I'd like ot make sure everyones line d up in the next week or so that we can have hte marketing team know each area that is being talked about and we can evangelize out to each area of the webinar, so please ping myself or naomi or both, let us know "hey yes, IU'm willing to talk about this, I need a full fifteen minutues, etc".  
*  Naomi - it will be on may 28th, 8am.
* Joe:  it will also include docs (perhaps we should talk about that too).

### Discussion - Sig-Release Chair
* Naomi - Speaking of release.. we had to open the Sig-release chair election again as Roddie has conflicts at the moment. If you're interested, please be sure to submit your name on the GHI!.

### Colinb:
* New AR system online fully?
* Joe: Right now both systems are running in tandem but we don't want to do that level of chaos during release.



