# TSC Meeting - 7/29/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L. A.
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Naomi Washington [LF]
* Nick_L
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* Tobias Alexander Franke [Huawei]

## Meeting Notes 

### Announcement - Matteo [Loherangrin]
* Stabilization starts tomorrow!  Noon UTC we will create branches and we will send a notification.
* After that, it depends on the type of the PR
* For the first part of the stabilization process - new features need an exception process.  We'll set up a board to ask about adding new features.
  Sig-release is going to define whether its safe enough to add the new feature to the branch or not.
* For all bug fixes, they are all accepted until the first soft freeze, we'll communicate the date next week.
* After that, we'll enforce the exception process for some minor bug fixes.
* Joe: If you need a second or 3rd opinion, feel free to ask me.  
* Joe: Also a strong chance, not 100%, but strong, that the particle system will be in sometime between mid and end august.  Maybe we can get it in,
  but there's a chance we can get it in for the release, if it shows up in time.  Its the #1 feature that people are clamoring for, we've been waiting
  for a year and it sounds like its getting realy close to coming in.  SIG-RElease people, Nick(Red Hat), Matteo, I'm happy to have a deeper conversation
  about risk vs reward, but anyways, letting you guys know its a good chance its coming in, we'll have to prepare for that.
* Jan Hanca:  One more question, do we have the same dates for o3de-extras?  still all the gems are there are optional.
* Matteo: Optional that o3de-extras is cut off the same day.  If you need more time, its fine.  You can track the main stabilization process after tomorrow.
* Jan: We're refactoring extras, splitting ros in to 4 gems, most probably we'll be working on the API for the next 2 weeks.  
* Joe: Please present in the next 2 weeks, give them your proposal for when you'd like to stabilize and freeze, and what your extras schedule is, you'd know
  how long its going to take and when its going to make sense.
* Joe: Because extras is canonical, its part of the release, but it can be disconnected from the release.
* Joe: We should document the plan where once we have a date we have a soft lock it is recommended that other optional repos and gem authors give us what their
  plan is in order to hit the release.  They don't have to tell us (3rd party is not beholden to the plan).
* Jan:  Since we know in advance we want a release in spring and autumn around roscon, maybe we can decide on cutoff dates in advance.  Of course, we can change
  the release date if there are major issues, but for cutoff we can decide it and announce it in advance.
* Joe: Only problem with that is if our postponement hits into the stabilization period for the next release it may cascade effect into the next release.  As
  long as release has flexibilty.  O3DE should have a release plan as far as dates go, and have dates on paper as far in advance as possible.  We have to be
  flexible since its mostly volunteers working and life happens and can affect the release date.

### Discussion
* Joe:  You jogged my memory on something we should do.  
* Joe:  We should publish a list of things we should push back on, like for exmaple renaming function calls and APIS, when not doing so is an option.
* Joe:  When the branch is created, it will dramatically affect users once we release, their QoL.
* Hellaenergy:  as you come up with the request/list and document htat so we have it and can review/act on.
* Joe:  I'm not going to make it, I can, but sig-release needs to take charge of or lead, I can put together a rough list, and I'd hand it off to sig-release
  and you can work your magic on it, then you can start running it by Nick and other SIGs.  Going to take a bit since people will have strong opinions about
  it, it should be linked in the main readme for all the sigs, of hey, here are the contributor requirements please think about these things when you contribute
  code.  That's what I'm thinking along.
* colinb[APMG] : We need a versioning system sooner rather than later, especially before the schema 2.0 stuff.
* colinb[APMG] : We are not enforcing the versioning changing on the objects when the objects change, its decisions that I and others made when we started o3de.
* Joe: we need to sync dev and release versioning, dev will be > than release, but its so wildly different right now.
   * Joe:  Put the 2 in sync.  come up with a versioning systme that puts 2 in sync.
   * Joe:  Enforce sigs to use versioning system to do those checks.  It does support range checks between versions, etc.  It supports people writing conversion
           code, they can auto convert it.
* Joe:  this might be WG material (temporary)

### Discussion - Discord Reorg
* Gaian has created a demo server based on https://github.com/o3de/sig-docs-community/issues/147#issuecomment-3120919521
* See the demo server, and please provide feedback.  They are open to feedback.
* JT: More and more discords are reorging due to the growth of discord and influx.  Like a rigging server just did a reorg.  Frequently, nowdays, they put
  them in an archive.
* Joe: I'd like to start making the changes by end of august if possible.
* Please do this homework within th enext 2 weeks (read RFC, visit server, provide feedback)
* Luis mad ea really good series of comments on RFC, please read over those and extend key points

### Discussion - Someone knowledgeable in O3DE GRaphics to attend Siggraph.  We will pay for travel and ticket.
* Anyone who wants to accompany me, please let us know.  We have a backup plan if nobody takes.

### Discussion - JT
* I got some follow up from last TSC. https://github.com/o3de/tsc/issues/152
* Community testing initiative is just an informal call for testing from community members.
* I wanted to get the big picture out today, and spend more time on the discord server reorg.
* Everyone here who's profession has worked with a QA team, etc.
* In open source, rallying community members is a little different, you have to have a consistent way to trigger them and let them know hey we're in a testing
  cycle.  We need a formal way to trigger people and have them follow a guideline and have them identify goals from people who produce the code, to focus the
  testing.  You define very clearly if you want functional testing, auto testing, (sig-testing), then tehre's perf testing, IOT would need security testing.
* The key is that I'd like to hijack the testing sig.  If we can integrate a little bit of this as an additive feature of testing-sig, we need a clear testing
  feedback loop 
    * Trigger (When to test)
    * What to test
    * Feedback mechanism.
* Please start thinking about that, I'd like to head that initiative.  I'd like to have it help with the october release, I can lead that.  I have extensive
  work with particle system.
* Joe: If you have this all figured out by august, great, but I don't want the particle system to be held back in any way due to it being a guinea pig for this
  new paradigm.  My intent is not to rain on the parade since I like what you're doing and agree with it a lot.  I'm very excited about it going in and dont
  want to delay it.
* JT: It has to be adaptable since there's a churn with community members.
* Joe: bounties?
* JT: Highly against bounties, negative against it
* Joe: And AI's have cuased major negative results with open source project sand bounties.
* Joe: I can't think of a way to motivate people to testing.
* JT: I disagree with the reward system due to the dynamics.  There's an organic way to do it, people get excited, a lot of programmers who love programming for
  games.  There's a lot of testers that can't do programming but they can test liek crazy.  They want to be a programmer one day, but meanwhile they can test.
* JT: Once we have it in place and have more testers we will solve a lot of problems.
* Joe: Naomi is part of many of the projects, maybe pick Naomi's brain, she knows a lot about how these things do this, larger foundations and how they tackle it
  to get their data points.
* JT: There's some real nuances with this being a game and content pipeline, really different motivation to something like kubernetes.  More DCC, web design 
  based stuff.  Always looking forward to talking about Naomi about anything.
* JT: Just want people to think about it, adaptability, reflection of the community itself, people getting to do what they want to do makes it more organic
  without any carrots or sticks at all.

## Discussion - Naomi - WG joe mentioned versioning
* In our community repo there's nothing that talks about WGs.  Its all about running SIGs.
* Joe:  I'm happy to write that document, and put it in front of the sigs/tsc for approval.  
* Naomi: I don't think we need to do it so formally.  We can just put a vote in front of the TSC and other SIGs.
* Joe:  the doucmentation isn't for this particular cas,e its for future cases, you or I may be busy, we can't answer the questions and 
  facilitate it, having docs there will help people self manage a WG.

## Discussion - Joe
* I'll be out at siggraph in tons of meetings from 8/10 to 8/14.  Won't be reachable.
* 14th and 15th available - then vacation, only reachable for emergencies from 8/15th to 8/26th.  count me out for the last half of 
  august!  If its an emergency, people know how to contact me.  She's a good peerson to contact, if we need joes input on X and Y, but only contact
  me in emergency - I'll be on a ship for a week and that automatically makes it difficult.


