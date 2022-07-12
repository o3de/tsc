# TSC Meeting 2022-07-12 Notes

## TSC Attendees

- Karl Berg
- Roddie Kieley
- Nicholas Lawson
- Jeremy Ong
- Tobias Franke

## Agenda

### [RFC Acceptance Criteria](https://github.com/o3de/tsc/issues/40#issuecomment-1181873398)

- Question raised regarding the acceptance criteria for an RFC
- So far, RFC acceptance appears to diverge slightly from SIG to SIG
  - One SIG held an informal vote over a period of time
  - Another SIG required chair and co-chair sign-off
- Generally, SIGs self-govern to correct for cases where the RFC process doesn't work for the SIG's needs
- _Action_: Some review may be needed to ensure the current process is working as documented, or if the official process needs to change or be written down.

### [Roadmap Publishing Discussion](https://github.com/o3de/tsc/issues/40#issuecomment-1181873398)

- Clarification was requested regarding the TSC's guidance on publishing a roadmap
- TSC uniformly agrees that publishing timelines with work items (even with quarter or year specificity) is ill-advised
  - Open source development does not operate on a deterministic timeline
  - Timeline commitments exclude contributors that can't necessarily commit to a particular set of hours
- Transparency is desired but should not over-promise on behalf of the community (not something we or the foundation can do)
- Other OSS projects avoid publishing concrete timelines for these reasons and more
- _Action_: Jeremy to reply to the thread on behalf of the TSC

### Question about licensing

- A question was raised about the licenses of various subprojects with O3DE, in particular Qt
- Qt being copyleft cannot be statically linked to O3DE and is not used in any runtime components
- Changes to Qt needed for the engine are also copyleft and open sourced in an O3DE Qt fork under the same license
- License approvals outside of the standard Apache 2 and MIT licenses go to the TSC, who generally requests guidance from the LF as necessary
- License questions for certain redistributables (e.g. Agility SDK, WinPixEventRuntime) still TBD


## Transcript

tobias
- do we have a min req for rfcs to pass?

ninepoints
- good point, will add to agenda

tomhh
- discored post
- teams updating roadmap items
- thoughts on that from tsc
- priority
- things to include / not include

ninepoints
- how good of an idea is it?
- should discuss
- in particular
-- blender, clang, gcc, whatever
--- generally give direction but not a "roadmap"


- tob's q on rfc min for acceptance
- don't believe there is a threshold
- sigs determine on their own atm on how this happens
- 

tomhh
- my understanding needed a min of two maintainers from that sig to approve


np
- 2 reviewer quirement for pr's and stuff
- but not sure on mandated standard for RFC's
- nothing technincal that enforces it

geds-dm
- sig-core has chair and co-charit sign off

tomhh
- per sig rules?

np
- is it 2 maintainers
- is it chair/co-chari
- vote then quorm across group?
- sig-graphics previous chair
-- effectively signed off on it
-- had a vote
-- last call for objections
- seems like no single way that's being utilized
- documented? don't know
- can make it a homework question for us if that's ok?

tobias
- reason for Q
- sat with tomas
- wondering if anyone were to come into the community and start pushing rfcs
that contradicted each other or would be hard to get into the system or whatever
how does the process of the review take place
- what min req.
- maybe a rebuttal phase or something like that

np
- if that's happening
- chair/co-chair have a lot to say about how the sig is goveraned
- part of the sig review is part of that governance
- royal would know best likely as he set this up
- use those existing mechanisms first if there was an actual issue


tob
- will try to think of a mechanism I can propose

joe b
- early stages of project growth
- need checks and balances so that folks can't come in and abuse the system
- haven't seen a problem so far
- solution looking for a problem?


tomhh
- we have req for strucring work
- could add those we have in progress to the document that was requested to the discord channel
- any additional details that the tsc thinks should be included
- roadmap includes times and dates
- those don't necessarily get delivered by a given date

joe b.
- talking to nicole and vincent about this
- pushing back
- something that o3de and lf wants to put out the users / partners
- quarter most granular we provide
- other engines just say we're working on this

np
- think even doing quarter even too much
- making promises you can't keep


joe b
- can't release a roadmap without legal disclaimers

np
- open source way
- can't stipulate a deadline
- will feed back to nicole and vincent

roddie
- impt. to have clear direction and goals
- but corporate commits to dates but not 


nick
- partners like amazon or red hat can decide and communitate time committments
- but not as the foundation and the community

np
- imgui branch from 2018
- tons of discussion, issue closed, and branch and discussion continue

nick
- like the imgui page that talks about features in development

karl
- back not committing to times
- people lose interest and focus changes over time

tobias
- roadmaps
-- for blender and godot
-- how does that work
- if for branch, if not active, when abandoned?

np
- eg. blender geometry nodes
- open discussion being worked on
- but no time committment as to being done when
- being abandoned?
-- will happen in large scale open source development
-- if branch goes stale all will know, but do need to close it?
- participants are folks you don't control in any way shape or form
- a branch may go inactive for months but then be picked up by someone else


joe b.
- maybe what's been done? what's being worked on? where we're aiming to get in the future?

np
- aspirational but not firm committment


tomhh
- in progress
- on hold is also a good state
-- if jump to something else for now
- potentially 'planned' if in the near term

np
- aspirational
- call for help?

nick
- on hold no reason if branch in repo and what folks to jump on and complete a branch's work


tomhh
- advise against or not have it at all

nick
- use on hold where the weird case that it isn't being worked by original author, but don't want someone else to be picked up


np
- 2 ai's
-- need help / help wanted
-- OR calling it out as it's something that the sig is going to work on later

joe b.
- did I capture that right?

tomhh
- yeah I think so

geds-dm
- 'not actively worked on'

np
- for sig to put out comms that something is not actively being actively worked on
- a bit presumptive for the org to state that
- needs to be more intent behind such a statement


tomhh
- concrete ex. a feature we worked on, view bookmarks for storing camera locations
- but ux not very good
- would like better ux
- no one doing anything on it
- if more resources would be awesome to have someone working on it
- would be useful that no one is working on it
- 'if you wanted to pick this up that'd be awesome'

nick
- way to say it is 'help wanted'
- contributors wanted
- low/med/high complexity
- here's the code, here's the status

joe b.
- things we would like to get to
- improvements to possible system

nick
- if someone is looking to contribute and has an itch in taht area
- a wiki page about it's state and what needs to be done
- just because you start the first few lines of the feature doesn't mean it's your feature


tomhh
- makes sense
- some of the wording and comms regarding the roadmap
- maybe just wait for vincent and nicole to update the wording to set expectations correctly regarding timing

joe b
- putting items in for the project manager but not putting in any dates
- going back and forth with clair vincnent on dates
- want to avoid dates in general

np
- dates not just our issues
- but ppl in community would not want that


joe b
- share roadmap doc with np and discussing what this roadmap should be
- sig-release has been discussing it

np
- sounds like pretty uniform consensus at this point



np
- royal assuming he's travelling and will do bug bounty and feature bounty next week

joe b.
- will be adding a propoal for new sig to manage assets
- more projects and demos
- need place where they can be managed
- posting that up with the kind of the sample of it's overview
- ppl can comment on if we can have a sig or not
- b4 next tsc meeting

geds-dm
- q, on qho manages licensing of a particular product in the repo
- issue, have forks of other open source license repo
- all licenses aren't mit/apache
- eg. qt
- which group for formal reviews of licensing


np
- default policy covers apache2/mit
- for projects outside of that forked or brought in 3p or otherwise
-- exceptions ok'd by tsc
- initial audit reviewed by LF legal
- which includes qt

nick
- if it's a new thing that LF distributes needs to go through LF legal
- link to open discussion #7

np
- would come to this group then we delegate to LF legal
- need folks that can weigh in legal advice and then make a decision
- when royal back we can ping about this


geds-dm
- concern, if we fork a legal repo

np
- you mean copyleft?
- need to be under same license

geds-dm
- if we fork a copyleft then build binaries, what's the effect?

nick
- generally you need to ship your changes
- very impt that we don't cause any kind of copyleft that would trigger a video game sources to be have to be released
- if it's an executable, and it's standalone, then we have wiggle room
- but if we make no mods
- copyleft does not apply to files you make with a tool, eg. blender

np
- thanks for the summary

nick
- legal often runs into problems with engineers who are attached to a given implementation that may be for example gpl3 which is off limits

nick
- when looking at a project, look at the license first
- we need to be focused on apache2/mit
- not compatible with our users
- copyleft not bad, can be a force of good

np
- is the q, just how the license files are placed in the repo?
- repos may not handle dual-licensed well


geds-dm
- qt with gpl that we forked

nick
- foundation not quite happy that we're using qt
- have to compile it as dll's and have to link it in
- executables have to work under the lgpl license
- got a special LF exception
- should be avoiding if possible
- a pain to work with correctly
- have to be very careful how you use lgpl2 and lgpl3 on your customers who are just trying to make games
- can't link qt into anything that folks want to ship as secret source like game runtimes on consoles

geds-dm
- since we forked it lgpl
- we can make mods to the forked repo?
- as long as we don't distribute libraries?


nick
- if link to statically, ie. compile qt static and link to it
- will trigger lgpl regular copyleft
- can link to the routines safely but need to publish the modifications made
- the modifications have to be under lgpl
- best case is not to modify it
- basically if we had another choice of another ui toolkit we might take it but too many years of work in doing that

np
- does that address the question geds-dm?

geds-dm
- yes

np
- roddie chair next week
