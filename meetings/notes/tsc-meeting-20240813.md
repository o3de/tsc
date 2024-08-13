# TSC Meeting - 08/13/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* LegacyOfWax
* lsemp3d
* Michał Pełka [Robotec.Ai]
* Naomi Washington [LF]
* nick_l
* null [Meta]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Agenda items
Agenda Topic: https://github.com/o3de/tsc/issues/136

## Announcements
* Joe: A reminder that we are a month and a half from 24.09 release.
* Joe: I'm looking for a volunteer to do stabilzaiton -> dev volunteer.
    * Joe: It requires someone who is familiar with the process.
    * Joe: There will be less to integrate after the first one, and we should be feature locked.
    * Nick: I'll do it if nobody else can
* Joe: I'll be out to a conference in the opposite time zone to the US.  Responses will be delayed next week.
* Naomi: o3de connect is tomorrow.
* Joe:  I'll have more announcements after the Hong-Kong conferences next week.  
* Joe:  we are prepping for october (ROS CON), which is big for o3de.
* Joe:  Steve, Sid, I'll be reaching out to talk about ROS CON for prep and make sure we know what demos we're doing etc.

## Topics from Agenda

### Topic from agenda - OpenUSD in O3DE
* Sid:  I can give an update.   We use assimp to import other format types like FBX, GLTF,  TinyUSD isn effort from opensource, Assimp added support to convert USD into Assimp.  They integrated that work from TinyUSD into assimp.  We integrated the new version of assimp which has that support, into o3de, and it works for really simple USDs.
* Sid:  We did find a bunch of issues with more complicated USDs, like if you have layering, variants, etc, we reached out to the Scene Importer people are saying its not them, its TinyUSD that didn't add it, so we contacted TinyUSD, they said its not them, its the Scene Importer that needs to call the functions correctly.  You need to add it properly.  You have to say "Load the variants", each layer, each composition, etc.
* Sid:  what I've asked is a RFC, the RFC will capture 2 things - the current working solution, then all the issues with it, leveraging other peoples integration. We'll create bugs, add basic support, etc.    Games don't use complicated USDs.  We'll get the robotics folks to offer some standard USDs that they use.
* Sid:  We will have a second solution in the RFC which has a much deeper integration.   Hopefully the RFC will act as one central place where the conversations happen.
* Sid: I took a look at where the feature missing here, is it missing here in the TinyUSD, or the way we're calling TinyUSD in the scene importer, we can open the bug properly, etc.
* Nick: My understanding is that there are optional nodes in the USD which are either no-load by default, or optional alternatives to switch between sub USD and scenes, and without specifying which scene to switch to or load, it won't load.
* Sid:  since this is a predominant use case in simulation space, let's get some prominent use-cases in robotics and see if they work.  If we may need to introduce a config file, etc, then we can have that discussion.
* (Technical discussion about USD)
* JT: There might be a RFC coming soon for more native USD support (USDZ)
* JT: I produce content and train people, I tell the USD people its all about the workflow of the artist and the team, on signoffs, etc.
* JT: Rainbolt had a lot of options for USD.  He might be available to consult with from the UX/UI team.

* Steve P:  Quick note - stabilization nightly installer builds have been failing.  
* Joe: When that happens reach out to Mike Chang.  
* Steve P:  I'm looking into it.  


