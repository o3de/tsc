# TSC Meeting - 4/2/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Gaian Helmers [Genome Studios]
* Joe Bryant [O3DF]
* lemonade-dm
* naomiwash_lf
* Nick_L
* null
* RoddieKieley [Red Hat]
* Sid_Moudgil [AMZN]

## Agenda items (Ad hoc) 

### APMG Colinb[APMG]
* I have the free assets that were from the linux foundation
* I have been starting to do the conversions on them.  Its a lot of work.
* Joe: Conversions?
* colinb: Sometimes there are only a MA file or sculpt and they need to be exported to FBX/OBJ
* Joe:  ETA?
* colinb:  Just gotten them, got thru most of the commandos, started the marines, they are in a worse shape.
* Joe:  Go ahead an put each one up as you're done.
* colinb:  Just trying to make sure that everythings in a unified format that makes sense.
* colinb:  THe store is working, so that's where I'll put it.  Also trying to get more work done on schema 2.0 for the object model
  Its been taking a lot longer than I hoped.
* colinb:  The licenses for consoles is still in-flight.

### Progress / prefab workflows - Gaian Helmers
* We are doing prefab work, doing a preliminary look over the maestro timeline things.
* Identify the most crucial pain points, look at problems with the work flow, features, tasks, needs.

### Joe Bryant:  Release in April
* Release in april will be a very small release.  Its hard to cherrypick features out of the release branch
* Mainly bugs plus performance optimizations around the asset browser.
* Once this is done we will create the next main stabilization branch off dev
* Probably going to take 3 mo to test this big release, so we are aiming for release in august/sept.
* Lemonade-DM: Whats the naming scheme?
* Joe:  Bug releases are point releases, so 23.8.1 will be the point release.
* Joe:  If we release a major release, 24.9.0 release
* Joe:  we saw a large bump in traffic during and after GDC.  We also saw a 22% increase in starred repos.
* Joe:  We can see that in github.

### Joe Bryant:   Gaian (Helmers) is in the process of becoming a community manager / advocate in O3DE.

### General Discussion
* Carbonated has ideas around systems - so like, memory, etc.  Maybe push them to have them in discord or publically,
  because Nick, lemonade-dm, etc, are the ideal people to have these discussions with.
* JOE: Changing core parts of O3DE, those must be public conversations - every training I've taken for LF have said that big decisions for OSS projects must be discussed public.  Start as early as possible, the feedback you get early on will likely change the details.
* Gaian: If its as simple as making a thread and fostering a timeframe etc.  
* Joe:  they should approach the sigs.
* Lemonade-DM: is there a way to back a Discord Thread up to github somehow?
* Gaian Helmers : At least breaking it out is great.  Need to be an ettiquette to post the link.
* Joe:  We haven't cleaned up threads, but they are ephemeral - we need to clean up or they become a big maze.
* Sid: one reason that the discussion is happening away from discord - one is that they are still working on the game and under NDA
  The other reason is that there's the ease of use of talking to the internal team on Slack instead.  I've been trying to push it, 
  but it would be easier to have these conversations in discord without divulging secrets.  It may make sense to keep pushing (Joe).
* Sid: Mostly they think that this discord is a long term thing and they need immediate resolution due to their deadline.
* Joe: They can do what they want in their own fork and code base, if changes need to go public, then the RFCs/discussions/etc would need to happen.  Its not super advisable for them to drift away from O3DE, but I understand the pressure, I've shipped tons of games and quite a few on mobile.  They are on that last 3-4-5-6 months phase which is hard time, every minute matters, so maybe what they do for now is we get their mobile stuff up, they just get to work on getting the game out the door, don't worry about github.  Once they ship and can take a step back and get past their first 2-3 weeks of support and emergent issues, they can start getting their custom changes into O3DE.  
* Sid: In this case, they are not worried about getting their stuff into Development, right now its just addressing their immediate issues.  Most of this stuff is in rendering, and in many cases they need something quick and dirty and mostly advice, not code.
* Joe: I don't want us or the community to be giving them complicated long term advice, they just need to get the game out the door.  
* Sid: They mostly want validation of their design decisions to make sure that their hacks or their tweaks are okay, whether they're on the right path.  
* Gaian: To these more broader topics, I didn't think that they would have such success but having such a name as "prefab workflow" threads have encapsulated a lot of issues / ux workflow problems.  This "prefabs threads" becomes all this discussion about prefabs in general with a long lasting impact.   Maybe have a Memory Management thread / etc?
* Joe: They are super concentrated on whats comfortable for them in their last mile of dev, so its going to take a lot of convincing to get them to enter discussions for long term.
* Joe:  Some projects wish to be on Slack as well, but I don't want to split the community.  I give it a low chance that we'd do it but I have gotten so many requests, I would be remiss if I didn't at least investigate.
* (A discussion about searchability and discord/slack)
*  - Maybe we can export threads from discord into Github Discussions?

- (Gaian Helmers) when we're deciding to do a thread maybe don't make it so exact?
* We could perhaps make standing threads that stay open for sub-topics of a SIG.
