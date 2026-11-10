# TSC Meeting - 11/10/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* ChristianHinkle
* colinb[APMG]
* hex
* Jan Hanca [Robotec.ai]
* jayrulez
* JT[SCB_Networking]
* Mike_C [Amazon]
* Nick_L
* ross
* Shauna [Genome Studios]
* sid_moudgil [Amzn]
* Steve P [Amazon]
* u78PL

### Announcement - JT - Moved the Connect meeting to next week
* Connect meeting is on the 18th
* 8am PST

### Progress on last week's action items
* Audio middleware topic
* AI WG

### Discussion topic - Hardware contribution - colinb
* There are ways to donate machines and do it in an absolute
  safe way.  Even if you want to dedicate resources to building, with
  isolation.  
* Shauna - Non-mac runners can be done in docker containers
* colinb: Its own login, cannot break out of its shell, you can run
  the github runner.
* Arbiter:  we call it o3de-labs.  Combinatoric of last 10 clang compilers
  and linux versions.  we have a VM builder that builds those inside to do
  internal testing.  Could expose that dashboard for PRs.  Do builds and 
  publish the dashboard.
* Mike_C [Amazon]:  The agent it runs assumes that you have a clean environment.
  Whatever Github publishes as their OS image you have to try to match the spec
  and github has licenses for things like vs enterprise, and you'd have to match.
  There's definitely some ways we can solve this, in a safe way.  If we're just
  doing it for testing purposes, its not a huge issue about the results of that
  run, although from a security standpoint, its arbitrary code running on that VM.
* Recently there's been attacks on dev machines.
* Mike_C:  I'm thinking more future world where we can seperate tests out to have less of a build the entire airoplane discussion, which reduces the threat surface area.
* Mike_C:  If there was an allow list we could definitely think about how we could perhaps layer this in a way that initial test checks out so that its not malicious and then when we start deeper testing it can go into a deeper stage.
* Mike_C:  Other build orchestrators to handle the build.
* Move to SIG-build and move to LF to ask about machines to use.
* JT: Mike, I have a question, I'm working with other groups and getting sponsorships for stuff.
* If we can get a sponsorship that can help us out with this?  Would it be the
  same thought to move it back on to their help and back to github?
* There are companies that say they sponsor o3de engines and give mac hardware
  and mac online stuff.  So while I'm looking for other sponsors that can help
  foot the bill.  If they decide the same way would it be too hard to move it
  back?
* Mike :  We can't tie ourselves completely to it, we have to find routes to
  move off it.  Sponsorships do not come for free.  There's always something
  they want in return.  There's legal discussions with LF.
* Ask the Support Group about the linux foundation sponsorship.
* Mike_C:  Initially my target is to get onto resources owned by linux foundations.  Organization member support.

### Arbiter - Announcement
* PhysX update need some eyes in case they break their stuff.

### Follow ups on prior initiaitves
* JT - Action item last from last week, update
* (WWise, other middleware).  Gaps in o3de.
* We kicked around some ways to word it.  We'll soldify it and start the 
  thread on SIG-All.

* Shauna - AI WG
* https://discord.com/channels/805939474655346758/1567229469356466316

* colinb - Scheme 2.0
* https://github.com/o3de/tsc/issues/159

* Shauna - QoL focus
* 27.10 release being the goal for optimizing the QoL
* we spend this time figuring out what kind of things go into the initiative
* Encouraging people to prioritize those.
* Shauna - Lots of workflow optimizations can happen, too.
* If we can get those prioritized, to target 27.10, then they would be beneficial.
* JT: There are some known, scrumpy, arbiters group, they are noticing unoptimized code.  We can extend and maintain it better and add to the little parts that inch their performance up.  OPS can be included.  Templates that Gaian has been working on.  All of that can cause a person to trip over it.  
* ross - bugs - assimp 6.0.6 - I saw that and I have another pr
  and I updated some of the dependency issues that have a 3rd party package
  and see if thats a direction we want to take things.
* After that discussion with WWISE - with engine changes we needed with WWISE
  we could include wwise portals, the audio system interfaces have to adapt.
  We use the latest WWISE.  
* WG don't have to have voting or anything either.
