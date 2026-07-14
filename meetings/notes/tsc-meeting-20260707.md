# TSC Meeting - 6/7/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Cheddarspice [Iamjbq]
* ChristianHinkle
* colinb[apmg]
* Hellaenergy (Nick) [Red Hat]
* hex
* JT [SCB_GameDesign]
* Kyler
* Matteo [Loherangrin]
* Mike_C [Amzn]
* Nick_L
* Yaakuro
* Shauna [Genome Studios]
* Steve P [Amazon]

### Announcements - JT - I'll help out with the translation packs
* I've already started the Qt thread, and I started a thread in sig-content.
* I'll get something up on github in the next week or so, so I can coordinate it.
* I've done it professionally in the past, worked with instruction manual translations, I'll help out.
* I'm condensing the documentation, and once we get a few language packs going, there's a massive global
  community that works on this.  I'm in touch with several other countries, india, others to coordinate.
* We do our part, and people come out the woodwork to do translations for us.

### Announcements - Cheddarspice [iamjbq]
* They have released 2 more Major Versions of physx since I went away
* I'm not sure the status of the AR for 3p package, because physx build creates its own build environment
  and doesn't use standard compiler stuff.
* Steve P: In the yaml file in 3rd party you can set up all the tools that are necessary.  But for packages
  that are special one offs, we add a setup itself into the build script, because these are running in virtual
  environments that get spun up each time.
* Cheddarspice [iamjbq] - What about checking before they are committed?
* Steve P [Amazon] - you'd have to look at the platforms, specifically.

### Discussion - Removing Slices from LyShine colinb[APMG]
* Its going very well - I've leaned a lot on AI to help me do it (its a lot of work)
* I have it kind of running right now, its not ready yet.  I've pushed it up to my fork.
* If anyone wants to take a look at it they can.
* Looking at how the AP was working.  How on larger systems vs smaller systems.

### Discussion - AP slowdowns / hangs
* I happen to have a fairly large system - and it was acting kind of funny and hanging a lot
  and having a lot of build errors and timeouts and things, and looked into that.
  I made a couple of changes there, but, it seems to scale a little better, so I'll put up 
  for PR.  
* Not a massive change, it takes into account some thread contention, auto adjust number of
  jobs.  I reduced the number of threads per builder a little bit.
* I implemented a ramp-up, starts with 8 builders at one time, looks at the cpu/system
  resources (cpu, thread contention, etc), if it seems acceptible it ups it a bit more, etc,
  and ramps it up, or down, depending on system.  The overall result is not that much
  faster than how AP runs, its the same, maybe 10% faster at most, but I was able to reduce,
  32-36 errors during full build, and now I'm down to about 2.  The usability, I adjusted
  thread priority based on load on the system, lowers the priorities a bit, (normal/belownormal)
  so it doesn't affect the rest of the system.
* I also multithreaded job creation, so that it can get thru the jobs faster.  Processing
  the jobs was taking a long time.
* colinb[APMG] - it times out a lot.

### Discussion - Engine Finder / schema 2.0
* colin:  The schema 2.0 stuff is way too large to merge piecemeal.
* Maybe we make a seperate repo.
* Shauna: One of the things I was thinking about was we could at least start cleaning up repo.json in 
  o3de-extras, at least start making it compliant with some sort of spec, if its schema 2.0 or some other
  spec.  Its better to not even have it.
* colinb: I think we should abandon 1.0 or go to schema 0 standard, something that isn't aggregating all the
  children info in the parent.
* Shauna - I took the repo.json and looked at each entry, its supposed to have a repo entry or "where to go
  to download the thing" entry.  Go find/calculate the corresponding gem.json file, and pull that and use
  that as the information for getting the information for release notes and all that.  Right now, thats
  difficult to do due ot the way its designed, coming from web development and rest stuff.
* colinb: Any o3de object root describes that object.  We do support parent-child relationships within
  and object, it has hundreds of gems, each project has gems in it, those object dont need to be registered
  themselves, the parent knows about it.  
* The root of everything is the o3de manifest.json - toplevel parents are the registered ones and know them.

