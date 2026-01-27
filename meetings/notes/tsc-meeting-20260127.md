# TSC Meeting - 1/27/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* Naomi Washington [LF]
* Nick_L
* NnN
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Hellaenergy (Nick) [Red Hat]
* We will be releasing 25.10.2 - slight bug fix for VS 2026 fixes

### Announcement - Move the Connect Meeting to this week due to joe being sick last week
* Joe is feeling better, connect is tomorrow 8am PST

### Discussion - Naomi - SIG Chairs/CoChairs discussion
* We used to maintain a document in a google sheet where it had all the sigs listed and all the co-chairs
* Last maintained 2023, but we probably need to refresh this document.  
* Sharing document (link hidden to avoid robot searchability)
* We did an exercise where we checked each sig, and made sure that they were up to date
* We cannot just promote people to chair/co-chair without process, since it gives them access to keys.
* We need a co-chair for TSC, we probably want to find someone who knows the engine fairly well.
* Nick_L Maybe someone from huawei or robotec, they are entangled with the engine.
* Joe: We need Graphics & Audio Chair/co-chair, its high priority and important
* Naomi: we should contact Anton (Current co-chair) to see if we can move on electing a different co-chair
* Sid:  Its so specialized, we probably need a candidate before we open, and then move on it.  However we can open it in
  the chat, ask people if they're interested, etc.
* Joe:  If you have a date, it forces people to make a decision.
* Joe:  We should talk about sig-testing, and sig build.
* Sig-testing job is to oversee the core test framework.
* Sig-Testing also maintains a checklist for a test team to use.
* What we found is that the sigs do that work.  There is no generic testing system that covers sig-network, sig-graphics, etc, 
  they are all covered by those areas.  We need to do some reserach to see if its truly inactive, and if so, ask each sig, 
  add to their charter that they're responsible for testing in that area.
* What I've seen so far anecdotally, is 75% of testing convos happen in sig build, the remaining 25% happen in various sigs
  for the particular area, like, sig graphics and whatver.
* colinb: we should specify which sig becomes responsible for decisions about the testing system itself.
* Joe: We need to also talk to sig-build / Mike_C about that.

### Discussion - Steve P [Amazon]
* Mimalloc allocator.
* We need some benchamrking, but mark the PR with the actual benchmarks required.
* Startergame (Editor) - Load and run
* Multiplayer Starter Game - Load and run
* Combinatorics:  HPHA+Mimalloc, HPHA+Malloc, Malloc Only, Mimalloc Only

### Discussion - colinb - o3de's public policy about AI
* We need a policy
* JOE: 
* TSC and the Board (Naomi) need to discuss.
* We need to add a slide for AI usage.
* My stance is that AI is a tool like any other tool out there.
* I could care less if O3DE contributors use any tool to create code or assets.
* I want to make sure its not going to conflict with IP, Copyright, etc.  Anyone who creates an asset with AI, 
  they should make sure its created with AI, and people can do extra checks around copyright.  AI itself, its easy
  to stumble on IP rights, much easier with AI than when people generate art themselves.
* What several open source projects are doing, there has to be a human in the middle.  When someone is using AI
  to create code or content, they have to have a human involved before it gets the PR submitted to check whether
  its sane, its not wasting time for putting a PR up for people to review.  Getting a lot of junk code up, of course
  if someone does that a lot, they will probably lose their contribution priveleges at some point, since its just
  noise.  we should not discriminate about how the code or content was created, we need to ensure the quality bar
  and it should be the same as every day contribute.
* Roddie: In a given PR, its 1-3000 lines of code, and depending on what model, depeding on subscription, most do
  not tell you where the code is coming from.  Maybe cite which LLM used to create the code?
* We should not limit code just because its created by AI.  Thats where everything is going.   we can't stop that
  train, we might as well prepare for it.
* Joe: Maybe we should have an AI Working Group to set these boundaries and rules for O3DE.
* We would never prevent AI usage with O3DE - people can do whatever they want with O3DE, always.
* But we can have rules and expectations around contributing to O3DE.
* An area where we have to embrace AI is documentation.
* Shauna [Genome Studios] - Especially for getting aroudn the "blank document" problem. 
* Joe: I was doing some AI for comparisons between O3DE, Unity, Unreal, etc, and the o3de side was woefully
  inadequite and out of date.
* Joe: Please leverage the redhat contact.
* colinb:  I'm making a replacement for program manager (Project manager) - I'm using AI to create it, and the
  program manager replacement has AI in it.  Its running a model and talk to it and have it create projects and
  gems for you and all of that.  
* Joe: Do you want it on the road map?  
* colinb: I'm still playing with it, so I have no idea when its ready.
* Joe:  The roadmap dosn't target any specific dates, just a list of things that we want to tackle and show progress
  in tackling.  We can put down "we are putting project creation and building be AI driven so that it can be AI
  driven and people can put what they want in"
* colinb: Its going to be like a AI that you leave open and it can talk to the editor as well and create things
  and put things in there.
* Joe:  you've piqued my interest, super interested, but please send me a small paragraph about exactly what
  you are doing.  It will help people be interested in O3DE since AI is such a buzzword right now.
* Joe:  LF has announced a foundation concerning AI.  we could leverage that as well.
* RoddieKieley [Red Hat] - MCP may be a dead end for a game dev POV but across the industry its what they
  are using.  But the context and the context protocol part has given you access to the data, not everything.
* Shauna [Genome Studios] - My contact, the best route with MCP is making sure you have a solid def. of what
  you want it to solve and be very deliberate about what you're looking for and what you expect it to do.
  Too easy to get caught up "lets do this thing" and get caught up with a fuzzy view of what you want it to solve.
* colinb[APMG] they would for example make MCP for interacting for each of hundreds and hundreds of commands, 
  your token usage goes up 10x, its not very good.
* Joe:  we will create a  WG that is focused around AI, and we'll focus on **contributing** to o3de using AI,
  and then secondly , how we want to integrate AI with O3DE, we want a plan regarding what we want to do with 
  AI long term.
* JT:  My work, once you get locked into it, you can't get back out of it.  Once we started, we could not 
  detach it from the code.  Be aware of that caveat.

