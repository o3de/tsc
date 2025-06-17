# TSC Meeting - 06/17/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andrè L.A.
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* Jack420 WARDADDY
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loharangrin]
* Mike S. [Carbonated]
* neighborlee
* Nick_L
* null [Meta]
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]

## Meeting Notes

### Announcement
* Joe: Today is release day, 9:30am pt, please do not speak up during the runbook for the release
* Joe: June 19th, there is a LF office closure.  You won't see Naomi or myself.

### Discussion - Discord topic:  An idea to create a channel for requesting reviews, PRs submissions
* The idea has merit, however, when I look at the stats, we are doing pretty well on our review
  and submission times.  I have access to the project dashboard.
* Nick: What is the actual problem we are attempting to solve?
* Joe:  People were complaining that their PR wasn't reviewed in time.
* Nick: Its likely due to lack of reviewers, not lack of knowing that they are their. People are
  volunteering and haveing day jobs.
* null [meta] - we should have a single reviews board for now.  As many eye balls as possible. First
  get a new channel and when thats too noisy then split it.
* Joe: time is averaged 4 days between PR create and submitted.  thats realy good for an open source
  project.
* Joe: We'll collect and present stats.
* Joe: People are forgetting to add their sigs and tags in too, make sure that they are listed.  That
  and the reviewers.
* Colinb: Make sure to tag.
* Joe: We should add 'needs triage' to every one.
* colinb: make sure you're doing your process on both repos.

### Discussion - Discord topic: People were skipping the requirements documentation
* The only hardware requirements we had listed was for minimum requirements, and minimum is not a
  great experience.
* When you go to download O3DE its more in your face, you see hardware/software and we supply the 
  information about to install it, directly in the download page.
* With that is the minimum requirements are basically limping along with o3de and you're not going
  to have a great experience if you have large assets.  One of the things I'm thinking about is
  raising the minimum requirements with 16gb.    They can try with 8 but I'm seeing people with
  large assets struggle with 8gb.  16gb is strongly recommended.
* Hellaenergy: We are kept honest.  People can know!
* colinb: We have notes that are more nuanced, you can do it on 4 sure and if you have a dual core
  processor, then that combination will not overload the machine.  You could have a threadripper
  with 64 cores and only 8gb ram.
* Joe: Supporting those minimum specs does increase our userabase considerably.  The size of your
  project determines the level of hardware you need.
* Joe: I'll talk to JT / Shauna about it.  Size of the project indicates how much memory you need.
* colinb: please add sig-platform.
* Mike S: Do we use any PCs that are minimum spec?  Most of our dev machines are more recent within
  the last 3 years, we are not developing for PC.  Anecdotally on certain machines that are much
  older we have found various performancei ssues.  6-8 year old machines.
* Joe: I'll talk to echo game labs about the systems they use.  They have extremely detailed game
  so I'm curious about what their experience is based on the machines that they use.  
  I called out Mike S becuase they're working on a big project, so they have the size of assets
  for a commerical project.
  Echo labs is making a PC windows game, they have extremely complicated assets.  So getting
  feedback from those companies that are using O3DE in a commercial setting.
* Mike S: If any of you have quesitons about features or perfs, if you'd like to provide those 
  questions to me in text or in the discord channels I can pass that to my engineering and art
  teams and get a response from you guys.
* Joe: Unreal has 3 recommnedations (minimum which is similar to ours), recommended (also which 
  is similar to ours) and what they use for commercial productimon 256gb ram 64 core threadrippers
  which is too much and I don't htink people care about that.
* Sid: I just joined but are we talking about CPU or GPU ram?  Its cheap you can have more.
* Joe: In some countries.  O3DE has well over 250k downloads and we are downloaded in over 100
  countries.  About half those countries do not have easy access to modern hardware and lots of
  ram and that sort of thing.  RAM isn't actually cheap in all locations.
* Joe: I think we need to specify if you are compiling the engine you need to upgrade to 16.
* colinb: we should output an absolute minimum hardware spec.  
* Joe: I think we should split it out:  installer version: 8gb.  If you're building the engine
  you might need a stronger cpu, need more memory.
* colinb: Programmers machine?  ARtist machine?
* Joe: Might take a bit longer together but a good idea.
* Joe: I'm just getting a lot of message about people unhappy its not working with 4gb intel integrated.
  Getting that info in your face when you download will help a lot.
  Previously it was mostly links.
* hellaenergy: What makes unreal better than us?  
* Sid: complexity of pipelines.  
* Sid: We can get there if people contribute back.  huawei has a nanite-liek pipeline, but they have put
  a huge amount of investment in there.
* Sid: As for AI, its nowhere close.
* Joe:  like for unreals case, they probably have between 2000-2500 people working on unreal.
  We have a lot of contributors, well over 100 fairly active, 500 sporadic, but, we can't compete with
  paying people 350-400k a year to work on the rendering engine or scripting tools.  Its the downside 
  to OSS.  The upside is that we have a pool of passionate people that come to work on it.
  With O3DE vs unreal, they have a lot of fringe tech we don't have, like a really complex animation
  system, muscular skeleton system ,etc, 
* Mike S. : My first position was on an unreal title, and I've shipped many unreal engine 4/5 titles.
  This is the first non-unreal title, non unity title, first open source engine in 10 years.  Specifically
  as a developer thats worked in unreal and is working on o3de that its a huge game, there is
  unreal engine 3 didn't start off with these, now 5 has things like unreal insights, UAT, guantlet,
  EQS, gameplayability system, niagra, nanite, lumen, they are not as big as some of the other things.
  Don't conflate developer experience with lack of features.  Comparing yourself with unreal is the
  wrong or misplaced way to look at things.
* Mike S: epic has 11,300 employes, with massive amounts of support, due to being profit company.
  People are drawn to O3DE, Godot, other engines, the big draw tends to be the community but it also
  tends to be the pace at which and transparency at which those engines work.  One of the most
  transparent people in epic, is just hte one outlier.  A lot of devs are drawn to him, but epic
  maintains a very closed loop of community and harnessing the power of the community to build 
  something.
* We strategically chose O3DE, we work, we can reach out to groups like this, to work with you guys
  on solving specific problems we have.  Its a level of support that epic has not given since opening
  UDN for unreal 3.
* JOe: I talked to several companies, what people like about o3de - the license - they can do whatever
  they want with no strings attached.  You see source code, its all transparent.
  Our modularity - modular from top to bottom.  UE and U are both fairly monolithic.
* Mike S: our top reason was strategic and licensing related.  Being a game developer now is so 
  radically different now from how it was 20 years ago.  It is extremely difficult to drive a profit.
  The second reason is the amount of interaction we can have with o3de contributors.
* Mike S: typically to access the UE5 / UE4 UDN you have to be a licensor and its so bogged down
  with buerocracy and process.  ITs honestly more appealing to AA and AAA sized companies and a lot
  less to the 30 person and below companies, 2-6m rev companies.
* Halleenergy: I'm observing a lot of hate for AAA games.
* Mike S: Its probably true, the sentiment is down, but probably off topic here.
* Joe:  Top 3 selling points for o3de.  Modularity. Licensing.  Renderer.   Best open source renderer
  period.  Every year it makes leaps and bounds in quality and performance and features.  Lot of that
  is due to the modular architecutre.  
  Joe:  Fourth is closest integration to Robotics Operating System (ROS2) period, compared to anything
  else out there.  With all the other engines out there, they require a bridge but O3DE ROS2 talks
  directly to ROS2 without a bridge and directly to the engine.  Our performance is  in some cases
  3-4-500% faster than unity or unreal becuase we don't have that bridge.
* hellaenergy: What would the naysayers be?
* Mike S: it usually is hte feature related stuff, but good devs doing this for a while can always work
  around that kind of things.  There was a great amount of work on things like trackview.
  It was all feature based wants, usually.
* colinb:  I hear most often in the negative column, documentation.
* Joe:  JT and Shauna doing their best to shore it up.  Its not as sexy as a new rendering feature
  but its extremely important.
* Colinb: its come a long way and like the engine, its got a ways to go.
* Joe:  Every engine has its strength, unity is eg easy to use.  Getting 80% of your project done
  is super easy.  Unreal is features - lot of features, lots of AAA -style features, cinematic
  so they are populare with production there.  But they keep changing terms of service and 
  licensing.  When you get to 100% in unreal it looks phenomenal but it takes a while to get there.
* Joe: For o3de you don't have to worry about the licensing.  Our rendering does not have all the
  features, but you don't need all the features.  Complaints at recent conference about all these
  unreal features that get in the way and sap perf.
* Joe:  O3DE has its strengths, growth areas.  Unity and unreal too.  Developer has to look at what
  works best for htem.  They're all good engines, not going to say any of them are crap, they're all
  good engines.  We are learning from it, but I can't just assign people to do stuff.  the SIGs
  have their roadmaps and then they try to convince people to work on things.  In open source thats
  how it works - we find people who happen to be interested in in the area and they do.  Like last
  year we contracted 4 devs to work on various parts of the engine, but it realy depends on budget
  and volunteers.
* Sid: The modularity of the renderer - been working on Huawei to work on multi-gpu.  The main
  engineer showed alt-frame render, eg, rendering 1 frame on one gpu, 1 frame to the other.  He
  had a demo where 12ms to 6ms, 60fps to 120ms.  this is on very complex task to do and its only
  possible to do on O3DE, all the original authors who worked on the original renderer moved
  into a different tasks, but yet outsiders can still implement these very complex tasks in the
  o3de framework, without being the original authors of the engine, due to its modularity.
* Joe: You can look atha up on our youtube channel, for the future of O3DE, we are very aware
  what is out there.  If our sole goal is to compete with unreal and unity we will lose, but
  we are instead doubling down on our strengths, not ignoring our growth areas, but measuring
  them and seeing where we get the most bang from the effort.
 