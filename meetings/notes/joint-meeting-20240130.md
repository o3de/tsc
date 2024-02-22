# Joint TSC : SIG Meeting 01/30/2023

# Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (by discord name)
* colinb[APMG]
* geds-dm
* Joe Bryant [Amazon]
* JT [SCB_GameDesign]
* Nana yellen
* Naomiwash
* Nick_L
* null
* Nicole Huesman [LF]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

### Recorded Meeting
* This meeting is recorded, for exact wording see recording.
* recording at: https://drive.google.com/file/d/1hKtObQUIyXwhk2Y8LlXiXWwYPOu8rjBy/view?usp=drive_link
* The rest of these notes is a brief summary.

### Overall outline
This is the "All sigs" check-in and roadmap review for the end of November.

### Agenda Topics
Github meeting issue: https://github.com/o3de/tsc/issues/109

#### SIG Updates

### Sig-Core Roadmap
SIG-Core Roadmap: https://github.com/orgs/o3de/projects/31
* No updates

### Sig-Platform - Steve P
* Steve P - ubuntu 20.04
* Dropping official support for 20.04 - supporting 22.04
* Joe - Adding 24.04 soon
* Steve P - we always have 2 versions - no more than 2, so as we pick up 24.04 we drop 20.04
* Joe: 24.04 is less than 4% of the audience, and we need to give a heads up.
* Joe:  Give people as much of a heads up as we can, ~3 months.
* Naomi:  Email nicole.
* https://github.com/o3de/sig-platform/issues/72 is the criteria.

### Rendering - Sid_Moudgil

#### OpenXR (Sid)
* Meta is adding full support for input for rendering, input being an asset.
* Its going to be completely up to the person who created the asset who made the mapping for the device
* They will add quest2 / quest3.  Anyone can add others.
* Not rendering input - so controllers, gestures event mapping.  This data drives the input mapping system
  for XR devices.  
* Its mostly done - will put up PRs very soon!  This week or next week.
* Even in december, this person has been updating openXR quite a bit, how it perceives depth, how it updates, very little latency.  On Quest3 it looks and behaves a lot nicer.

#### on Huawei rendering tech (Sid)
* We will nudge people to use that automated rendering test framework.  We'll nudge people to test using the existing automated testing.
* The framework is there, the documentation isn't there.  I will probably write a quick wiki page.
* spirv-cross needs to be updated on mac and windows. Don't really need it on windows and linux.  We don't really use spirv-cross on windows or linux.
* spirv-cross is for cross compiling on one platform to another.
* colinb: Mac isn't officially supported.
* Sid:  Problem is IOS, not really mac.  We need ios functional.
* colinb: we need build coverage
* Sid:  Its extremely expensive.  Perhaps we can just buy a mac...
* colinb: We came to the same conclusion, maybe we can use jenkins to build a trusted mac instance.
* Joe:  Its super expensive.  Over 6 mo you already paid for an instance, and there's very few providers
* Joe:  we'll just get a mac and support it.  With an AR, people will submit prs and test locally.
* colinb:  Also, we have to decide whether we support M1 AND x64.  The issue is just capacity / 3rd party.

#### Joe - Sig-Network
* Focusing on reducing the size of server builds.  Influences several sigs.
* Managed to get a 10x decrease in size.  Brought the multiplayer sample from 4 gigs to 450.
* Its assets, going thru everything and stripping assets for server builds.  Within 30 days or so PRs up for those.
* Steve P:  Headless is the terminology, rather than server.

#### Joe - sig-Release
* Today I will be talking about handling releases for o3de.
* looking at our current resources available, I'm not sure it makes sense for us to do a LARGE release several times a year.
* Some large projects, they will make smaller projects and then one major release per year, with smaller releases throughout the year.
* Resourcing is going to be difficult for that.
* Naomi: Release early and often - more point releases, releasing early and often as well, and because resources are so thin, its better for the team.
  Its not been easier for the last 2 point releases.
* Joe:  One in december, one in january.
* colinb[APMG] - vote on it?
* Joe:  Schedule a sig-release meeting, if you have input join this meeting, and we will 2x year start that planning and scheduling.  I want to report in this meeting.  If you have input, attend the 10am meeting today.
* Nick: Advertise it or people won't attend

(see discussion on recording)

### Ad-Hoc topics to bring up?

#### Naomi - GDC 
* We are going to GDC!
* 200sqft booth, we're in the hall with godot, oppo, I'll post the location, we're in a sprint since its just around the corner.
* I think we're going to be doing something similar to what we're doing in ros-con, let you all know that...
* we have a number of seats available, reserving it for GDC and can give a live demo in the booth, if that's something you're interested in reach out to me, we are trying to maximize the impact of our presence.
* Swag related question:  T-Shirts at roscon, I have been partial to hats.  The perfect drawn to the booth hats.
* (Everyone seemed to love hats).  Shirts are required for booth worker.
* Sid - let's try to get the mobile work in to the dev branch before GDC, that way you can say at GDC, it works well on mobile.
* SIG-Release branch or release for this?  
* Joe:  We don't have the testing resources to know that dev can be stable for GDC.  A lot of the contributors are getting ready for GDC as well, huge distraction.  Primary user that is helping us get mobile together is not ready to start submitting to mid to late feb.  Wary of trying to plan that for GDC.  We should announce it when its in dev.
* colinb: the velocity in dev is not that high, so maybe we'll be ok.
* Naomiwash
* Actual conf 20, 21, 22 march
* build out is 18-19-20 march

#### ColinB - RFCs
* https://github.com/o3de/rfcs/issues/52 - Reorg O3DE
* Maybe there is a better way to do releases - we group everything into two giant repo (o3de / o3de-extras).  
* We might benefit from slimming down the O3DE repo, if we look in a certain direction its a lot more visible to have the program manager
  (Project Manager) - o3de.exe - the repo would only be O3DE and thats what you build and release. We should then be able to release individual objects (such as projects, engine, and so on).  Strip the engine of almost all of its gems, the AutomatedTesting project, the templates, objects we host instead.   The project manager would be able to fetch and construct them.

* https://github.com/o3de/rfcs/issues/53 - Update o3de objects to schema 2.0
* Schema 0, Schema 1 was added by alex,  I propose schema 2.
* Joe: Please ping Alex on this.
* colinb:  Engine objects are the engine object itself, anything that has engine.json, template.json, restricted.json, gem.json, project.json, they are all named objects and can be referred to each other by name.  Objects have dependencies (by name).  It can have children, so engine can have gems in it.
* restricted objects should be considered renamed
* Joe:  Impetus for this, platform addition?
* ColinB: Yes, APMGs primary target is console support.
* ColinB: this is not a breaking change, 0 1 and 2 are backward compatible
* ColinB: There are different sub-schemas for different objects.  Schema2 would be to try to standardize all them.
* ColinB: Project manager would show you a list of all the available versions.
* ColinB: Confusion or conflation between repo.json that describes a composite repo, and an advertisement for project manager (locating objects on the internet. Formalization of this - repo.json vs advertisement.json.  Describe in the document why and how thats differnt).
* Joe:  Don't equate project manager == o3de, its a tool for o3de, o3de can be successfully used without ever going into the Project Manager.  
