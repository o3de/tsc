# TSC Meeting - 7/14/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* colinb[apmg]
* HellaEnergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* JT [SCB_GameDesign]
* Kyler
* Matteo [Loherangrin]
* Nick_L
* Shauna [Genome Studios]
* Sid_Moudgil [Amazon]
* Steve P [Amazon]

### Announcement - HellaEnergy
* We have started planning for the next release.
* We are targetting october.

### Announcement - Colinb
* I put up the replacement for LyShine to be a prefabs system.
* Its not new functionality or anything, its just a conversion over.
* Tried to be respectful of reviewers time, so there's two parts
* One is a mechanical copy of LyShine Gem and Examples gem.  I manually copied and dropped the Ly so its just Shine
* Bulk is in 1200 changes, but the meat is in part 2, which is the movement over of the slices to prefabs.
* We dont need slices when we get rid of this.  It will just be after this goes in, if it gets accepted, we can
  do a pass and remove slices from the rest of the system.
* Going to put a third gem in, called LyShine To Shine conversion stuff.  You can activate it and convert your stuff.
* We can have that there side by side for a while and we can set it for deprecation.
* We could try putting it in an external repo instead
* NickL: It could be a case study for moving it to another repo and find pain points for developers working on
  the modularity of the engine.
* Hellaenergy: Are we talking about taking something out of extras and moving it elsewhere?
* NickL: No, this is the development of a new gem that is independent of the other gems.
* Colinb: Maybe moving this one system is a good test, really trying to nail down the pain points and trying to
  solve the problem proactively and restructuring the core.
* Colinb: We'd need some way to verify binaries, perhaps that we can prove that the source results in that binary.
* If shine is a stepping stone for that, I would only consider that route when we had 2.0 in place.
* Its going to need its own versioning system, that has to be fully up and operating.  We could talk about breaking
  pieces of schema 2.0 before it comes online, like the versioning stuff.  If we had the versioning stuff in place
  in the engine, I would feel a lot more comfortable about keeping shine out of the core.
* Jan Hanca: I wanted to say that we need to separate the different gems, and atom is a basic renderer but there
  are definitely lots of gems in the core repo that are totally optional.
* There is a draft PR from early 2024 that was opened by Alex P with some gems being moved to extras.
* Jan Hanca: At robotec AI we distribute gems in binary forms, we inject the source code of gems into the engine
  folder, we add them to the list of directories in engine.json, and we simply build the engine, and then the
  files are there for monolithic build, non-monolitic, so on, we distribute them as libraries as headers, and
  everything in the engien supports that easily.
* Probably if we do it correctly, without the fake injecting, with the tools in the engine.
* JT:  I've been working on this for minimum install image.
* JT:  MPS / Minimal Install midterm goal.
* colinb: When you get into replacement for the restricted code system, for example, needs work.
* colinb: Whether or not we want to separate out PM from the engine.
* colinb: separate the CLI out from that as well, it'd more like an AWS CLI, you install it, its own project.
* colinb: Overlay objects / patches are a concept too.  Code assembled into layout -> correct files you want.
* colinb: support for any compiler/change.  A lot of times you are using a lot of other peoples code, and you
  cannot wait for uploading an upstream change back to the source, hoping for another release soon, you patch
  the code locally and go with it.  The overlay system would facilitate that without changing the underlying
  source code.  We could add platforms that way that are restricted.

### Announcements - SIGGRAPH SUNDAY
* Siggraph starts on sunday (this week), I'll miss tuesday's meeting probably, but I'll be working with 
  ASWF and the collective project we're doing with ODIE and USD this week.  I did something crazy and got it
  to work. I'll update after siggraph, and will be recruiting people to help us with USD, from the USD community
  while at siggraph. Starts on sunday, monday, tuesday are heavy days, wednesday thursday are exhibits.

### Discussion - Sig-release
* Matteo:  For SIG-release its imporant to choose a date, according to roscon event that is this year
  is in september, not in october. We try ot be close to a roscon event to have more visibility we think this
  time it will be a little bit difficult to realize everything for september, we will like to discuss this
  with the Robotec.AI team, if theres a constraint that requires us to release next to roscon for october, 
  without other issues.
* Jan:  I will discuss it internally with my CTO, who will be presenting there, and AMD, so it will be quite
  a big thing.  I'm not sure how much of O3DE will be there, I will double check it and let you know.
* I am aware of the date for ROSCon should not change for o3de.  If we do anything with O3DE for roscon
  we will present the release candidate and it will be fine.
* HellaEnergy: Is there any robotics simulation work you're trying to get into this release that is still
  outstanding?
* Jan:  We are doing something (secret) in parallel that I can't talk about right now, but it will be related
  to multiple engines, not O3DE specifically.

