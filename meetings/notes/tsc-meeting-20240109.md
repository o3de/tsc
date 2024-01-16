# TSC Meeting - 1/09/2024 

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* nick_l
* colinb [APMG]
* Naomiwash
* RoddieKieley [RedHat]
* geds-dm [Amazon]
* Sid_Moudgil [Amzn]
* Steve_P [Amazon]
* null
* Joe Bryant [amazon]
* Nicole Huesman [LF] 

## Agenda items

### Agenda Item: Naomi - 2024 Roadmap - 1st half of the year
* Naomi:  We wanted all of this done by Jan 9th, but I wanted to make sure we were on the same page, open the floor to anyone to add anything.  Nicole has been waiting for this to build a marketing plan around it.
https://docs.google.com/spreadsheets/d/10HN_XwanPA2jSGJZIUcud53iyYjtWcCS7Jkq6_4lipo/edit#gid=0
* Joe:  Working on it, February is way too packed and I will be moving items across to March, april, May.
* Joe:  A contributor is looking at porting lumberyard demos over to O3DE. I don't want to be the only person dictating
  what the roadmap looks like.
* Naomiwash:  Anything missing that we'd like to see on here?
* colinb: I'm working on the object system but don't have a solid date.  I don't have a RFC for it.  Its to help support a store integration.  (February timeframe?)
 (The TSC discussed this for a while and worked on the above link.)
* TSC Discussed next ubuntu LTS release date.  The platform SIG should discuss this.
* The plan is to support 22.04, 24.04, and to deprecate 20.04
* The announcement should be reported as an impactful change, and communications about it.  Joe to work with Nicole.  Or colin can work with Nicole on how ot message it.
* Scope is unknown.  Somewhere between not having to change much except a few build scripts all the way to having to ship a bunch of 3rd party library rebuilds.
* Huawei is under-represented here.  Sid: But they have many teams and they are all different. They all have different roadmaps and teams.  Sid to reach out, and see if they have any items.  Huawei shows up to the board meetings too.
* Colinb: Should we have 24.06?  Joe:  Yes, we are trying to get 3 releases per year.  Even if its just bugfixes
* Nicole: It would be great to know which of these should have broader community support on?  Change the tone to be more humble about things, so it would be great to say 'we need help with this' / 'we're working on that'/ ... Are there other things to invite people to contribute to and help with.  Or we could put out more general messages about that.  
* Joe:  Particle Editor / systems.  Thats the last engine feature that is not supported with open source.  It would be great to have an open source particle editor that ships with O3DE.
* Nicole:  It could also be bugfixes.  
* Sid:  It says the march release is IOS / Android support?  Is it really going to be ready for february release?  The wording of it, that we are adding - they are just not as performant.  Add a mobile pipeline.
* ColinB:  Short term visibility vs long term?  Should we go just by quarter? 
* Joe: We can fill in some items for may, for example, lumberyard demo porting.
* ColinB:  Distribution of those assets could be done via the store if its online.

### Agenda Item: Naomi - Global Game Jam participation & action items
* Board has approved us to participate in the global game jam.  This is happening Jan 20-28.
https://docs.google.com/document/d/1RRURJT91l997SgG42DK5JCw6_VzfUYMlVSg5CXQg-gY/edit#heading=h.qto0d6g41aq8
* Once the contract is approved I can send this over.  I can create the discord/onboarding channel
* Joe: Onboarding videos exist but are not accurate.  Do we have time?
* Naomi:  Probably a quick tutorial that is clipped down and targeting the GGG.
* Joe:  Installation video, then onboarding video.  Can the foundation do video editing?
* (TSC Discussed whether a budget could be used for video editing.)
* Joe:  I'll get engineers (to record video and send it) but someone would need to edit.
* Joe:  Onboarding:  Cover the available systems and docs to read.  We don't want to dive into things like script canvas and so on.  Those could be hour long subjects just by themselves.
* Joe:  Cover the different gems and talk about audio / bare necessities needed to have a game jam product and how to get into script canvas.  How to use prefabs and how to export your project.
* Naomi: We still see value for being in the GGJ
* Joe:  GGJ is in-person only, not doing remote, and that limits the kinds of machines people can use for the GGJ.
* Nicole:  That's a good callout, I thought it was online, too.  
* Naomi:  We only see value if we have a large online presence, but if its mostly in location, its not really valuable. 
* Joe: Installation video must-have, onboarding video is okay, but onboarding doc is better.
* Naomiwash:  I will do a call to the general channel / tsc to check the discord channel.  
* Joe: I'll have a rotation to check the channel.

### Agenda Item: Naomi - O3DE Connect meeting - this Wednesday
* Naomi:  Next meeting is tomorrow - the time is now 8am Pacific, 10am central, 11 eastern.  About 4pm CST.
* Naomi:  Global game jam might need to be parked.  Tenative.  Nicole has lined up interaction toolkit.  Steven Harman is scheduled to walk through it.  The other folks we reached out to - Matteo Russo (Logherain @ discord), February.
* Naomi:  Material canvas?  Tenatively agreed.  We'll see if we can get a final.
* Joe:  Material canvas should be limited to 10 minutes (Sid: It could easily go for half an hour or more otherwise)
* Naomi:  Hopefully the time will be good for bringing in new members.

### Ad-hoc agenda: Joe Bryant - Asset release to community
* All the assets that were open sourced for Crucible are in the lumberyard format.  We can try to find out what to do with that.
* Joe:  100gb of assets that have been open sourced and given to the o3de foundation.  Tracking those down so that we can figure out what to do with these assets, but it seems like they're in a nebulous area right now.   I have them locally and can re-upload.  Levels, materials, textures, animations, assets, for the Crucible game.  Everything content related.  Already approved to be fully open sourced.  What I'd like to do is take all these assets and put them up somewhere and have the community take them and convert them.  
* Would rather do that than pay someone to convert them.
* Colinb: APMG store is online and working on the integration of the engine, I would like to host as much content as I can.
* Joe:  Its not intended for people to be charged, they are free.
* Colinb: Overl03de is a market and people can charge what they want (nothing if they want).  APMG will mostly be looking at console support.
* Nicole : There was a page already available but not public for an asset store.  
* Joe:  Scheduled for June.  We have to hunt down the assets.
* Nick:  What formats?
* Joe:  lumberyard format plus the maya/max files source.  Includes all the effects ,terrain, vegetation, everything.



