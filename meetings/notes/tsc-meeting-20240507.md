# TSC Meeting - 5/07/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
Adam Dabrowski
Guthrie [Amazon]
Jan Hanca [Robotec.AI]
Joe Bryant [O3DF]
Luis Sempe
Michal Pelka [Robotec.AI]
Naomi Washington [LF]
Nick_L
null [meta]
Sid_Moudgil [Amzn]
Steve P [Amazno]

## Agenda items
https://github.com/o3de/tsc/issues/123

### Agenda Item:  Future plan - Joe
* Joe:  I need to finish the roadmap - its not really based on what I want, its what contributors are actually getting in.   I need to figure out what contributors are getting in for the last half of 2024.
* Joe:  I think we need o3de to be "Game Jam Ready" - 2 features missing Game Jam Ready
   * UI For Project Export is missing
   * Second piece is particle system 
* Joe:  We have people creating stuff in Game Jam timeframes, you can check the showcase channel for some examples.
* Joe:  Can you evangelize working on something in O3DE - one of those two would be awesome to have someone work on.
* Joe:  For large project games.  That has a different set of issues to tackle so users can make large projects around O3DE.  For example the Asset Processor is an issue.  
   * Making it so that if you have tens of thousands of projects, asset analysis takes forever even if you make small changes.  
   * Getting a cache server up and running.
* Work is being done with Houdini from sideFX
* Right now I just want to get those 2 gaming use cases, I want to get some efforts underway and get them on the roadmap.
* For the robotics side, there are a couple things that need to be done there, I'll be talking to Adam about that
   * AI work that's being done, filling out roadmap beyond July on AI stuff.
   * I've seen a couple other suggestions and needs (splat maps, etc, I want to get a list from Robotec.AI).
* We will be at ROScon this year.
* Adam Dabrowski:  support for Ubuntu Noble 24.04. (Joe:  this is already on the roadmap).
* null:  (Meta) Selfishly for us its all about AR/VR, android device support.  Anything we can do there to get it working sooner, it will have a large effect on adoption
* Joe:  We have a couple items on the roadmap, but its the things that are missing I'd like to see a list.  I'm not an AR/VR expert, inform me the things that we are missing so we can get them on the roadmap.  I can determine a direction but its moot, if I can't get hte maintainers / contributors on board.
* null:  For our side, I pull in Anton and Galib.  They are both working on this.  
* https://o3de.org/roadmap/
* Joe:  I've taken to heart that the website for O3DE.org is not gaming oriented enough, its not games forwards on the website.  I'll do some brainstorming and talking and a survey during the O3DE connect meeting tomorrow.  We want to reflect equally between robotics and games.  More heavily oriented to robotics right now.
* Joe:  We're also trying to figure out the marketing for O3DE and revamp the process. Please fill out the survey if you can.
* Joe:  What I may do is in the roadmap, put in a TODO section that people can choose to take.  For new contributors to look at and take.
* Nick L: Importing assets needs improvement.  
* Joe:  It also affects robots, but that is tied to a lot of the processes that game uses as well.
* Nick L: we should focus on papercuts too.
* Joe: (will create the topic)
* Joe: I will be stating this at the TSC meeting every month.  remember, for me as Joe as ED I help establish direction but only maintainers can actually get things done and determine what happens.  I suggest, "this is where we should go", I report to the board and suggest where we spend money and get members into the foundation to think strategically, but everyone else here as a contributor has the real authority.

### Agenda Items:  Steve P [Amazon]
* Do we plan on publishing containers to Docker.hub?  What about github container registry?
* Its a way to distribute O3DE using containers.  Its particularly helpful for simulation, being able to upload containers, but being able to distribute o3de as a base container and a lot of their samples could be containerized.  So basically when you publish container to the registry on any linux system you can just run it... its an easy way to try out the demos without going thru the process of building the container locally.
* Joe:  It makes sense, the containers make it easier for deploying if you're using/consuming for cloud pipelines it makes it much easier too, the issue is the O3DE foundation doesn't implement things, its the maintainers and contributors.   If someone is willing and interesting to implementing and maintaining the container.  I will need to know if there's anything we need to sign, or certs we have to deal with, they would cause legal issues, but as far as the implementation its finding someone who is willing to do that work.
* Steve P:  I believe you have to sign up for containers.
* Joe: Having it on dockerhub makes it easier for other organizations to consume.
* Adam:  Interesting, I'd like to talk to steve about that.
* Joe:  Tuesday 25th I'll be back in the office
* Sid: Looking at an O3DE AMI, are looking at an AMI.
* Steve P:  Getting containers up and running in the game space - servers.
* Sid_Moudgil O3DE Marketplace AMI.
* Sid:  Unreal/unity removed their AMI.  There's basically no open source 3d engine if youw ant to consume 3d content on the cloud.  There's no quick way to get that set up.  We hope to get that AMI up and on the marketplace.  Else you have to build your own container and pay them.
* Side note:  It doesn't have to be just container.  we can in the future think about other packaging and distribution systems.
* winget ?
* chocolatey is another consideration.  Meta also uses chocolatey.

### Agenda Items: Sid_Moudgil [Amzon] - Mobile pipeline is merged
* 24 fps shaderball to 80 fps
* You still have to build the variants, which we may disable by default.  It does add quite a bit of overhead and maybe we disable it for if you're not interested in mobile?
* Once the content is built, your variantlist can be built, 1k to 1m per variant.  Its project specific.  It starts taking a lot of space and takes more processing time to get more variants.  If you only care about VR, we can do an on the fly build and thats, metal and vulkan supports it, but not DX12.
* Something thats for future.  Shader variant system, we check in the mobile one, it has the most impact, since they have the least registers, etc.
* Before the variants with all the perf opt, we got 45 fps - we built the variants from scratch and it went to 80fps.  And its really hard to know, its tricky and we can give you insane benefits.  
* The first step is to crawl your materials and at worst you need 2 variants.  Its very content dependent.
* We do add some variants to some shaders, teh shaders that are not forward pass - deferred pass for example, we can only have 3 variants and put those in the core engine.

### Agenda Items:  Speeding up AP startup / building
* Colinb:  asset cache server.  Hierarchical list of servers?  Maybe a preprocessed list of server on the internet?  servers to look at?  Prebuilt assets?  A lot of countries (EU) charges per megabyte.
* Joe: We have (Gene) looking into the analysis phase.  Once we have that resolved, we can look into the asset cache server and have it work better with git.  It still updates the fingerprint on GIT.  The cache server needs to be a bit more tolerant.

### Agenda Items:  AI in engine
* colinb:  Don't want to pollute engine with the asset and not consider it open anymore.
* Joe:  I will contact the other orgs and talk to them about AI and the guard rails around AI.
* https://lfaidata.foundation/
* Release meeting in one hour.  Release is small (point release).  Not a lot of stringent processes in ploace for.  When I get back from PTO, we'll start the process for 24.9 major release.

