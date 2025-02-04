# TSC Meeting - 2/4/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb [APMG]
* Jan Hanca [Robotec.Ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Mike S. [Carbonated]
* Nick_l
* null [meta]
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* Tobias Alexander Franke [Huawei]

## Meeting Notes

### Announcement - Joe Bryant [O3DF] - New Release Chair
* Sig Release Chair is RoddieKieley [Red Hat]
* Co-Chair - Loherangrin

### Announcement - Joe Bryant [O3DF] - OFAC
* U.S. OFAC Global Sanctions restrict communication with certain nation states.
* Anyone operating in an official capacity for O3DF/O3DE must abide by OFAC
* Read, Ask question, then have each sig schedule with their maintainers to discuss this.
* Members can still use the engine, can still post a PR, but those working officially for the O3DF / O3DE cannot have a 2 way
  discussion with the members if they are affiliated with the sanctioned entity.
* It is important that we are aware of it and abide by it, because I am witnessing another foundation having lots of issues becuase
  they did not abide by it.
* The US Govt takes it seriously.
* We don't want a Police State in discord.
* We don't ask people where they're from, if they volunteer it from.
* Once we do find out we have to follow the sanctions.
* I want us to avoid the serious issues that another foundation is having.  
* If you are a chair or co-chair, or a maintainer, please read the OFAC sanctions blog, and then I will answer questions from it next tuesday.
* Its impossible for me (Joe) to schedule one meeting for all maintainers all over the globe.

### Announcement - Joe Bryant [O3DF] - next point release
* I will be meeting to talk about the next point release with chair/cochairs today
* I will be starting to work on the next major release, planned for May.
* Branch will be cut soon.

### Discussion - Jan Hanca - Google SOC project
* I didn't really find any response from O3DE community about O3DE in GSOC
* It would require at least 6-8 small projects for students to implement
* We don't have the capacity to mentor all of them, I wanted to mention that during FOSSDEM that happened last weekend
* I talked with a couple of guys and the good news is that most probably we will have 2 projects closely related to o3de
* One will be behavior tree related, implemented in O3DE, and somone from Robotec.Ai will be mentoring that.
* More importantly, we also started as robotec.ai, we worked with DroneCode, an open source LF implementation foundation for drones.
  This sounds very promising for me, most probably 2 projects around integrating PX4 into open 3d engine, probably o3de-extras,
  that means we will get some integration with drones.  Discussion is between DroneCode and Robotec.Ai.
* Joe: You made Naomi and I aware of SoC and the issue is the timeline.  If we had known in the fall that would have made it a lot
       easier to have mentors lined up, and right now there's not enough time to get 8 mentors lined up to fully participate in G.SoC
       with that, this is a lesson for next year, starting late summer, start the process for GSOC lined up.
       It does sound like Jan got people outside of Robotec.Ai to work, who is They?
* Jan:  The main contributor to PT Studio (Open Source Behavior Tree Library) - has Gazebo demos and GSOC will be porting those to O3DE.
        It will raise awareness of O3DE in the community.
        The One more promising was the one from DroneCode, Raymond, he is from LF, it would be integrating PX4 from drone code into O3DE.
* Joe:  For next year I want to start the conversation a lot earlier, get mentors, we have to submit by the 8th for the projects.  Way too
        soon.  Around July we need to start discussions for 2026
* Colinb:  Unless these projects or Gems have been approved by the LF they should not go into the O3DE extras.  Start as an independent
           repo and be evaluated by O3DE/O3DF.
* Joe:  Create a summer of code repo.  o3DE-extras has taken on the connotation of being maintained, sanctioned code.
        If its on personal github we could lose it.  If we create a foundation repo thats based around this, it has a less chance of us
        losing it because htey become inactive before we can pull it.  I'll talk to (Jan) about this.  The foundation could create 
        repos for this, and ask people to work in these repos for GSOC.

### Discuss - Nick - ASAN
* ASAN added to docs?

### Discuss - Nick - Prefab speed update.
* Looked at a while back and they didn't come up with a solution
* Poke some of the people (Danillo, etc.)

### Discuss - Nick - HPHA
* HPHA - Disabled it for some allocation.
* Colinb: Some systems are still horrible at malloc - off by default maybe?
* HPHA - Memory alignment.

### Discuss - colinb - Static Analysis
* Static analysis tools - filter / analyze.
* hand-in-hand soon we are required to do security analysis.  we can time those together.
* Because for LF rules we have to do a security analysis 5 years. 
* null [meta] - cry 3.5 - PGI - it was the same thing, that code was not designed to pass anything clean
  meant to ship specific titles.  going down that path you are going to get the whole sweater. 
* colinb: Even if it gets low hanging fruit its worth it.

### Discuss - joe:
* Cost for AWS has gone down, to less than a tenth for 2024.
* AR runs are less costing than before.
* We are still moving to github actions because we don't want to be subject to the generosity of AWS, as much as we like AWs
  People can run AR on GHA as much as they want and wont cost anything.
  We will be paying for storage.


