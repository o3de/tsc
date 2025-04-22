# TSC Meeting - 11/19/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Jan Hanca [Robotec.AI]
* JT [SCB_GameDesign]
* lsemp3d
* Nick_l
* Null [meta]
* Reece H [DrogonMar]
* RoddieKieley [Red Hat]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* Sunnny [Role Playing Studio]

## Meeting Notes

### Announcement - none

### Discussion - Sid_Moudgil [Amzn]
* Obj Support - I plan a PR.
* Sid_Moudgil - Something that is cool that I'd like to share, I was testing out a custom POC
* I was able to grab the point cloud gem and get it all working in VR, and OBJ came up, and also a Movie Player gem, from Carbonated.  I have discussed with contributing it.  Under the hood its a simple gem that makes OS API calls to load a movie file and pla a movie file, but thats all I needed.  I needed a very performant android version.
* Point cloud gem was having perf issues. 
* Sid_Moudgil [Amzn] - I had to download an external thing to convert the format .PLY point data with header
  at the top.  But other than that it just works.  Its not part of the core engine, and 2 features, was able to just grab a gem from other contributors.
* Hopefully the movie gets contributed back.
* JT:  I worked on a movie player for blender.  That'd be perfect, I'll add it to the notes.
* Sid: We used the same ebus, they just hooked in a different impl.

### Discussion - Sunny
* discuss the future of USD integration into O3DE.
* Sid_Moudgil - Gene is working on it, but I'm working with them.
* Sid: The current implementation is using Assimp via TinyUSD, and O3DE understands assimp, so its a one way door, tinyUSD -> Assimp -> O3DE.
* Sid:  we want to make this, the easiest and most impactful way without rearchitecting the entire internals of how the o3de system is set up.  now you have 3 dependencies you have to update, initially we had to update assimp, next thing gene was looking at was references.
* References are a more complex topic because it has to exist in assimp, and assimp doesn't - so it needs an update, then o3de needs to pull it in properly, etc.
* Sunny:  My vision for O3DE is that it can fill in a usablity gap in NV Omniverse, the messaging around omniverse and push for making USD the standard is that USD is going to be the new source format for content creation, but in practice because Omniverse does not have much in terms of content creation.  But O3DE could be a source format for content creation, and may be best for filling in the usability gap, could be for triple A game making and its open source.
* Sunny: I'm thinking of creating a USD scema that can encapsulate the .prefab filetype that we use in o3de, and then a bidirectional sync with all the product assets or files are being used in the asset pipeline, to create those product assets, syncing those with whatever the USD representaiton would be, would be the starting place.  Then one by one we update hte code module by module, instead of modifying the assetinfo for the scene description, we modify it to read / write from the USD instead.
* The easiest entry point right now is the cinematics pipelien, becuase the Maestro Gem is way behind, and so if we just start with making a USD native sequencing gem to replace Maestro, that can be the entry point into the process of first syncing everything to a USD native file and then gradually making it directly manipulate USD instead assetinfo or whatever else is creating those products.
* I'm looking at the docs for the AssetPipelien and looking at what exactly the user is modifying and what exactly the user product files change, and syncing whatever the user is modifying.
* If this becomes NVidia Omniverse go-to game engine.
* Omniverse Enterprise has additional bells and whistles, has bells and whistles
* The real money maker is that this allows you to connect your contnet to NVidia cloud services, train models, use models, etc.
* JT: Thanks to gene and sid (Galib?) at the last O3De-Connect meeting.  I did a bunch of promoting and got a lot of good feedback.
* Both the videos will be uploaded to youtube and understand how to use gamelift / and how to set up your custom render pipeline.  rendering based.  
* JT: I'm sure Naomi will upload it soon, and we have a written tutorial.
* JT:  I do lean documentaiton, internally, but I'll follow up on that later.

### Discussion - Reece H. [DrogonMar]
* The person that runs VKD3D that Valve uses (specifically the HDR person).  I talked to them about to try to see if
  we could update the HDR to vulkan backend.  Vulkan doesn't have anything that deliberately describes the color space.  But VKD3D converts it to some color space, and its perfectly valid.  Haven't heard any complaints for anyone using the Steam Deck and thats an OLED device.
* So far I've got some things working, vulkan does report the correct mips but it looks a bit dim.  I would like to see this going, getting HDR in vulkan would be great to get going on linux or steam deck.
* Sid_Moudgil [Amzn] - there is no P220 as an enum at a higher engine level.  The way it works is that at load time, it will ask the driver.  
* Reece H. The format I get when creating the window is A2R10 UNORM Pack32.
* Sid_Moudgil - first it asks the drivers what format(s) it supports.
* Sid: Then it asks what monitors
* Sid: Then it picks the best format based on the monitors.  Then it picks R10G10B10 and enables HDR.
* Sid: For Vulkan, you would have to all of this.  You'd have to make sure when it says "hey give me all the compatible formats".  it needs to have not just R8 but also the R10s. 
* Sid:  Then you have to connect the monitor that also suports R10G10.
* Sid:  then finally when you request the swap the texture from the drivers, then it should have HDR rendering working.
* Reece H. [DrogonMar].  So there's more to HDR on windows, than jsut swapchain cpp.  When I searched thru all the code, I've been searching for keywords.  I'm referencing VK-d3d and o3de's directx12 impl and I'm just bringing that to vulkan.  it would work in the same way that directx12 work on the steam deck.  They do work just fine.  I've had no problems running P220 games.
* I'm trying to get out of O3DE.
* I'm cross referencing the dx12 and referencing the vulkan backend.
* Sid: Maybe exposure went wrong, maybe we didn't apply the right exposure.  Perhaps there's a bug.





