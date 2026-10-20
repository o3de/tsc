# TSC Meeting - 10/20/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Astin(Chogan)
* colinb[APMG]
* ElPicaronCL | Sebastian T.
* Hellaenergy (Nick) [Red Hat]
* hex
* JT[SCB_Network]
* Jan Hanca [Robotec.ai]
* Jayrulez
* Nick_L
* RoddieKieley [Red Hat]
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* Ulrick28

### Announcement - Nick (Sig-Release)
* Still on track for next wednesday release date
* This week we'll be finalizing the release notes as of thursday
* Friday will be considering release stable unless we run into critical blocker.
* Found a splash screen - "Minecrafty dude"
* from https://discord.com/channels/805939474655346758/1553233142737801226

### Announcement - JT
* JT:  Went to 2 different gamesoundcon mixers/etc.
* We are getting some recognition.  But of course, fmod and wwise rule the roost.  we are getting some traction.
* 70-80 people spoke to.
* Ran into an ex-contractor for carbonated too.
* Time being well spent.

### Discussion - Sig Graphics-Audio-Leadership needs shoring up
* JT - ongoing conversation.  Recruiting people in southern california
* onboarded a senior android developer, learning graphics.
* I know that Arbiter - they've done a deep dive into Atom, and has some improvements online for atom.
* That is a basis for attracting graphics engineers that see ARbiter and other newdevs and see active posts and PRs / RFCs
  to engage the external community some more.  Put RFCS in for atom.
* Sid - I think that a lot of folks have been putting up PRs for graphics.  I think that those are good candidates to be involved
  ask questions, review others, a few of them are good starting points for candidates for this type of work.  With AI you don't
  have to have the pressure of understanding every single part of the core component that is being touched.  Opus 5.5 is great,
  if have to review that's what I'd do due to time and stuff.  Catch all the criticals and blockers and those are the ones that
  you are trying to address.  Majors and minors are up to your discression, up to this point.
* Sid - Give it like half an hour, it churns through the whole directory, churned how every component works, how all the materials and
  shaders worked.  I would never catch this for that pipeline, etc.   I would be pretty confident with running 5.5 on the criticals
  and blockers.  A really high bar, I've seen in the past.  The person who is managing and merging the code should be the one
  responsible for it and test it.
* Told my whole team, run agents/use agents but the person who is merging is responsible.  But don't be a blocker, we are no longer
  writers of code, being reviewers.  We are glorified testers now.
* Ulrick28:  Can you send a list of the people who would be good candidates who would be reviewers.  Your recommend pipeline for
  using AI for the graphics sig.  
* Sid: I've been using my work setup, so I'm not clear how that would work globally in a github setting.  Whatever tooling people
  have, like, claude or claude code, CLI API, but, use that and use 5.5 or above, its a big leap from the previous ones.  There is
  no magic thing here, we just have 
* (JT) Do we have any trackers that show how many tokens?
* Ulrick28: Maybe we can look into other foundation members?
* colinb[APMG]: I've done large projects from beginning to end (large ones).  I've hardly even looked at the code.  The velocity
  is like 1000x faster than we're moving.  The project is too low and velocity is too slow.  We should be using AI a lot more.
  Even Tim Sweeney - they are going AI overload maxiumu.
* Sid:  They got rid of blueprint / deprecated it.
* JT: They used the phrase "If they are not making it user centric, I'm not going to contribute my toolkit"
* BYOA.  Bring your own AI.
* colinb[APMG] If you're worried about tokens you should'nt be.  I work in it all day, every day, for the last years, and I have
  a subscriptions.
* Ulrick:  we need a solid policy for contributors, especially new contributors.
* USers will be responsible.
* We need guidelines to put down.
* We need to be about quality of life for users, not making it easier to contribute via AI.  IE, they got rid of blueprints because
  its not User Friendly.
* JT Its a bigger topic than we can handle in a topic like this.  Its easy to say what you want to say, or see what you want it to see
  if you elimiate it all.
* JT I've heard what everyone said but I wam working hand son with hundreds.
* ElPicaronCL: I use you are thinking about AI like work on I came up with an idea what might be viable. There are two respositories
  with AI stuff and one without.
* Ulrick: One version that has AI and one doesn't.
* Gaian has started a channel specifically for AI.
* We need a meeting like the TSC meeting, but where we speak about it specifically and I think its going to take a while to work all through taht.
* ElPicaronCL: My idea at the end the two converge into each other so they merge into each other.
* Sid_Moudgil:  Is there someone who can confirm the credits?

### Discussion - Stability pass for 27.10 release - Shauna mentioned it, JT is talking about it now:
* proposed Concerted stability pass for 27.10 release, and it was met with a lot of good results.  Would like to repeat it.
* We've never had an optimization pass for the engine ("Juice Pass") where we focus on optimizing speed and performance, where we take things that
  are slowing things down and speed those up.  That thought came up very strongly.  We wanted to seed the conversation.  Like last year we did
  a stability pass, maybe we can do an performance and opt pass between spring and fall.  

### ElPicaronCL : I just posted a gem about spawning entites.
* Its absolutely slow and unoptimized.  I haven't been able to find the root cause.
* Gaian and I have been working on it for over a year.  This would be one of the most priority things.
* https://discord.com/channels/805939474655346758/1562121738261766144
* Joe: Same problem at Lumbeyrard - they profiled for a week and found them.
* I highly recommend profiling.  The profiling is the only way to find a way to find out whats happens.

### ElPicaronCL:  I would like there to be a sig for VFX and CG
* Special effects / Virtaual Production.
* JT: compositing need to be in the engine, postfx.
* Filmmaking one?
* ElPicaronCL I wanna be part of it!

### Colinb: Schema 2.0
* Appreciate helps and comments, get a workgroup going.

### Next week
* Astin(Chogan):  Can we have a discusson for making Atom more user friendly?

