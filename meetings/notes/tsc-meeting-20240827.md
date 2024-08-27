# TSC Meeting - 08/27/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Gene [Amazon]
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* lsemp3d
* Nick_L
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* tobias Alexander Franke [Huawei]

## Agenda items
Agenda Topic: https://github.com/o3de/tsc/issues/138

## Announcements

### Announcement - Joe Bryant - Upcoming release
* Some times during September (3rd, 17th, oct 3rd) We are asking people to test the stabilization branch builds
* We will be keeping a board for stabilization branch

## Topics from Agenda

### Agenda Topic - AMZN-Gene - USD RFC
* Started an RFC for USD support. Comments highly valued!
* [o3de/sig-simulation#92](https://github.com/o3de/sig-simulation/pull/92)
* This is a push to get USD into O3DE.  Doing that in stages.  
* It could even be a potential replacement for prefabs, but there's steps in there where they are still
  useful for getting models available online, for example, nvidia posts a lot of USD files, that people would
  like to use inside O3DE.  Looking for feedback on that.
* (see the discussion at the above link)
* A lot of discussion here, about that, specifically variants and flattening.  See the RFC as the discussion develops.
* Joe: Asking about the phases, and priorities for the various phases.
* Joe: will include Gene in the NVIDIA USD meeting

### Agenda Topic - spham-amzn - Android monolithic libs to installers
* Adding Android monolithic-libs to the Windows + Linux Installers
* SDK never had android artifacts, in particular - android is monolithic only, I initially created one PR that disables Android for the SDK, but after finding out that it wasn't too much work to add it, I have another PR that will add the artifacts.
* The Artifacts for monolithic builds is release only, we can do the same for android, but android being that its monolithic only regardless of release or profile - is it worth it to add profile+release?  Without profile, there is no logging.
* Increase the size of the installer - release - 12.5gb , adding profile adds 5gb.

### Agenda Topic - JT [SCB_GameDesign] - Demo mode for O3DE
* JT is not present.  Encouraged those present to read the thread in the TSC

## Open Discussion

### Discussion: Joe Tutorials
* Contracted people to do tutorials
* We need tutorials, get lots of complaints, they are out of date
* We will be working over the next 6 months to fill in those gaps.
* colinb: We might want to consider AI generated, or updated easily without having to pay people.

### Discussion: Joe trip to Hong-Kong
* Actual event was wednesday-friday 21st - 23rd - I got there a day early, 30 hr trip each way
* It was a successful trip, learned about how open source works in Asia/Pacific region (China, Korea, Japan)
* For China, Open source is extremely important.  They build really large communities.
* Talked with Huawei - they are going to open source their particle engine.  They were going to open source other items.
* 3 different companies with 3 different implementations for Virtual Geometry.  None have open sourced, but one has said if nobody else does, they will.  I will work with sig-graphics/audio to get one of those solutions open sourced.  They haven't implemented their solution yet.
* Virtual Geometry is a star piece of tech in commercial engines like unreal.
* Robotec.AI - They're looking into implementing ROS2 on windows - one company is actually doing it - I plan to connect Robotec.Ai and that company (Huawei)
* Reports that there are problems with gems in ROS2 - Gaussian Gem.  A gem that they created themselves, but they are having problems with ROS2.  Discussion between Huawei and Robotec.Ai.
* Houdini follow ups.  
* Blender, I know who the integrator is for that, I'll reach out to them separately
* Lots of interest in OpenUSD from every company I talked to
* Editor translation tech.
* They didn't implement it in a way that is scalable or coudl easily be updated or scaled as new releases came about.
* I have a RFC coming up for actual translation layer for O3DE.  I've implemented localization before in projects, and it needs to be scalable easily used across the editor.  I suggest using AI to generate it.  
* When I put this RFC together, I expect to be the final version to be very different from what I suggest since there are people who know way more than I do.
* Huge learning experience to learn about that gap between the western and eastern side
* (Tobias) : There is unity and Unity china for example, they basically don't talk to each other.
* Joe: There are legal reasons for this, they are forced into this situation.
* AWesome trip, I'll be going again, travelling a lot.  I spend about 1 week a month travelling, to talk to potential contributors, get people interested in engine.  I had eyes and ears in gamescomp, but its very good for O3DE.  Typical NDAs with companies and such.  Let's just say O3DE is being used a lot more in games than we thought.

