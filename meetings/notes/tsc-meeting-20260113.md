# TSC Meeting - 1/13/2026

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L.A 
* Jan Hanca [Robotec.ai]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Matteo [Loharangrin]
* I would like to remind sig-release meetings will resume on tues 20th, next week.
* We have plans to discuss the 2 major releases and the second point release to fix vs issue.
* regarding the next major releases, the proposal for this year: 
  * One Major release every 6 month, starting from april.
  * Second one in october.  
* This will allow better balance between the development cycles.
* We plan to set the cutoff for april release to be the end of this month, but we will confirm the date
  as soon as Nick [Red Hat] returns from vacation.  The dates are already in the roadmap.

### Annoucement - Mike_C
* Impactful change sent yesterday - we will be switching from Jenkins to GHA as primary method by which
  we'll be validating and approving PRs on Wednesday.  
* Because its not really an issue here, but, the jenkins instance will be scanning for PRs, so if you
  do run it, with this switchover, it will show up in the status screen for the PR.
* Nick: There was an AR Punch-thru, is there a similar system for the new one?
* Mike_C: We'll simplify the punch thru and I can change the config so any of the chairs can punch thru.
* JT: Where do we put questions?
* Mike_C: Sig_build channel.
* Matteo: Are we also replacing jenkins for installer?
* Mike_C: This year we will be switching all that over to github actions.
* Mike_C: Do we want to make that public as well?  Generally for security purposes you don't want to expose
  your installer build scripts, it could open it to exploit.

### Announcement - JT
* I got to check in, in person, with the monthly indie game developer meetups in town last night
* Did some straw polling, had 50-60 devs, sound engineers, artists, and the discord I'm on with them
  is kind of slow.  They tend to do all their business in person.
* One of the confirmations, one of the areas being developed, especially in light of AI is narrative dev
  one of the coming jobs that is highly saught after, kind of like UX.   One of the things to look out for.
  Narrative design, I looked at some tooling of pulling narrative design content into the engine, like back
  story.  I'll pick this up when its relavant again.  It looks like narrative design is going to be robust
  and survive attempts by AI.
* Also, lots of sound engineers getting into the industry.  
* I passed out flyers, got in touch with a lot and talked in depth with several people.  
* I used the standard flyer.  Naomi, do they need to be redone?
* Two of the three QR codes are not functioning and are on pause.  Robotics is the only one working.
* Naomi:  I'll fix that now, I'll look example to right now.
* About 5-6 boutique studios that come to this meeting recently.  Its still watercooler talk.  I'll share
  other things as they come up in chat conversations.  People out there want to engage in community projects,
  the more projects we have to onboard people, the better.

### Discussion
* Mike_C - we probably need to get some of the mac packages promoted in, without some local testing,
  and no AR run.
* Nick_L:  I think its okay - the packages are built by a clean image each time using GHA, and the user
  does not submit any binries - the user submits the build script, and that script is reviewed as a PR,
  by humans.
* Steve_P:  Some packages may need to be updated for security, one of the things that came up for the arm64
  stuff, I could not compile anythign lower than a newer version, untested, etc.
* One package, for example, updating python again.  Python version we're on is end of support end of this
  next year, pretty soon.  I was not able to compile python version we have on arm64 mac.
* colinb[APMG] - Maybe we can use the find_package versioning for o3de.
* colinb:  GHA for mac builds.  Is there a way to trigger them?
* Mike_C: I'll be putting a PR in that will do a config in, and you can trigger it manualy for that portion.
* What about MacStadium (rent mac)
* Naomi:  I'll look into that
* JT: ASWF looked into it and there may be some way to glean info.

### Discussion
* JT:  Thanks for all the help with the community, from the communty!
* We got lua onboarding, etc coming soon, quick start template and lua docs is coming in.
* Shauna and I (docs stakeholders) are working on the onboarding documentation.  If there's something you need
  or you find something, jum pinto the docs channel and let us know that the dev documentation needs this, that
  or the other thing.  If there's anything we can do to help you all.  If you want to shadow nick and his 
  todo list, thats slowly spinning up.  thanks to steve for jumping in recently.  In the discord chat we have
  cheddaspice jumping into see how they get accepted.  I got to promote the audio stuff last night (reece)
  So I just wanna give thanks and let docs know if theres anything we can do to help.
* The docs are generally good, but the **onboarding** docs are not necessarily good.  Those are the parts of the
  docs we will be getting up to snuff for the next release, its just getting over that first hump.  If you
  see any of that stuff, ping us in docs.  Say "hey we found a gap and people are falling through the gap!"
  We have a lot of changes coming in the october/fall release.  We'll run that by the TSC.

### Discussion - colinb
* https://github.com/o3de/o3de-extras/pull/1016

### Discussion - Jan Hanca - O3DE Extras has no tests/moving stuff
* Maybe we can move a few not-always-needed gems there?
* We need to work on tests, for o3de-extras, and maybe we should consider back to this idea
  so that we don't ship the engine.
* We used to have the jenkins scripts, it used to pull in o3de.
* Minimal right now, it captures status quo, it was not included in GHA.


