# TSC Meeting - 9/02/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* jayrulez
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loharangrin]
* Nick_L
* null
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Joe - AMA September 10 wednesday coming up
* Send complicated topics ahead of time, so that Joe can do research.
* Please spread the word to everyone and anyone.  it will be recorded.

### Announcement - Jan - About O3DE-Extras - Cutoff for stabilization branch
* With the fix of Huawei we are able to test O3DE-extras against stabilization
  branch with the cherrypick of that fix.  We need 2 more days to make cutoff.
* We want to make sure everything builds correctly, and since we have some possibilities
  to implement in open source this week and last week.  We decided to rewrite one 
  outdated component since Simulation INterfaces.  We are still working on it, and
  have 4 developers and it should be done tomorrow.  And we will cut stabilization right
  after this PR is merged into development.

### Discussion - O3DE Extras release as part of engine
* Possibly for additional releases.
* Jan:  we want o3de-extras to be released togehter with o3de.  So that o3de-extras are seen as part of O3DE.
* Jan:  However, we don't switch our clients to the latest release instantly as the release occurs.
* Jan:  We decided to port a simulation interface back to 25.05.  We think releasing them might be beneficial for the
  community, so we can push it back to the main repo instead of the fork.  I'm aware that its impossible a 25.05.2 release
  but we have the internal version old old gems that are on extras.  we can basically make a release for the canonical
  repository and with this being said, the o3de project manager would be able to pull the newest gems and use them.
* The Only question is whether the community is ready for that.
* Joe:  Its possible to make a 25.05.2 release that is only the new extras gem.
* Jan Hanca - in Gem.JSON, we have internal versioning of gems, we can set those compatibilities, this already works fine
  and see when you start the project manager and pull any verison of the gem from o3de-extras.  
* Jan: From my perspective, if we want to release a new version of the gem, I need to push it to o3de-extras, and then
  push it to o3de-canonical repository, the only techincal problem is pushing the code to the github repo.
* Jan: We have a development branch for dev, and main for release.
* Nick: Can we just make a 2404Backports branch or something similar put it there, then have the actions zip it up?
* Joe: A lot of the functionality is already there, we need that working group to figure it all out.  We need that
  tsc and wg to have a look at the gems, figure out which ones are to have their own versioning scheme, and which ones
  are definitive parts of the release.
* matteo:  we have upgraded a gem that is already developed in main branch with something that is in development?
* matteo:  My point is if we add something as a backport, its something added in a previous version, and now we are targetting
  the main version.
* matteo: on our release cycle, we end support of the previous one.  In october, we stop supporting the main release.
* Joe:  Sig-release, TSC, possibly sig-platform, investigate how other engines handle plugin versioning vs main engine versioning.
  We may need to make a change to our plugin version schematics, but let's see how other engines handle it.
* Jan:  I will prepare a short doc and push it to sig release repo and RFC and explain the branching and techniques I want to use
  this is something we see every day in simulation area because many companies that support their products do so for a long time.
  Typically what I see in github repos is multiple main branches for this purpose.  There is often a separate main branch 
  for release 2409, for 25, for 24.10, etc, making new release of the old lts product.
* Joe:  typically companies charge for those, we wont, but if you look at redhat, canonical, they're all built around lts support.
  That means it has a guarinteed lifetime for bugfixes and support.  It's 5 years for LTS, with fedora, and ubuntu.  But if you
  pay its 10 years.  In film/video/gaming/simulation/robotics the large companies are not keen on bleeding edge, when I was making
  games we would stick to a verison of the engine that was usually, by 2 main version behind by the time we were released due to
  wanting to avoid risk in the release cycle.
  As O3De becomes more popular this will become more and more of a problem and we should try it out and see how this solution works
  and this is where sig-platform can come in with whats core and whats not, get its own internal versioning and not be reliant on
  the o3de main version.
* colinb: versioning is not related to where the gem was, its just up to this point we haven't been doing it.
* colinb: because a branch is cross cutting across all repos.
* joe: We didn't have the demand that necessitated the need for it.  This plays in for other companies I've been talking to as well
  which want to build things around LTS versions.

### Discussion - Current State of Particle System
* Joe:  We should not release it, we should put it in development.
* Joe:  We also have to have a discussion about preview, etc.
* colinb:  It is modular, it could be done someplace else like extras.  The communication of preview is somewehre else.
* Joe:  Experiemental, Preview, etc.
* colinb: we should put it into a seperate repo like extras.

### Discussion - Jenkins
* Jenkins is dead in the water due to a package built for a newer GLIBC (and new VS2022 CRT) on windows.  It works fine 
  on users machines who have VS2022 or ubuntu 24+ but not on older ones which jenkins runs
  

