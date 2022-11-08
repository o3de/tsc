# TSC Meeting 2022-11-08 Notes

## Attendees

- Karl Berg
- Roddie Kieley
- Nick Lawson
- Jeremy Ong

- byrcolin
- Finite_State
- geds-dm

## [Agenda](https://github.com/o3de/tsc/issues/58)

Agenda wasn't carried out in an official capacity due to lack of quorum.

## Miscellaneous notes


- looking for guidance or decision as to where new gems should be contributed to
- o3de repo or extras repo

- driven by robotics ai ros2 gem -< o3de
-- where to>

colin
- something I'm putting out hopefully this week
- that coincides with the AR update for o3de-extras
- decision tree component to it
- list a bunhc of questions and receive guidance of where things should go

nick_L
- that's good
- certain parts of the license and stuff that excludes
- want extras to just show up without federated repos
- may want federated repos, ie trusted repos, down the line

colin
- reviews e-mail that's going to go out
- explanation
- o3de-extras to be considered a part of the release
- therefor o3de-extras is a part of the distribution (?)

- streaming issues ensue

- sharing e-mail content that's about to go out on the subject

- explanation of what's going on
- part of AR for o3de-extras going online
- will be part of the release
- AR will run on it
- goes through what that will mean
- once fully online
- need to think about what objects go where
-- which go into extras
- from an AMZN perspective
- who owns the object
- or does LF own it
- if AMZN owns it
-- eg aws gem
--- needs own separate repo, not main, not extras
- is object large or small
- composite repo both are
- engine is top level object
- engine
- template objects
- if too larget should not go in a composite repo
-- meaning many megabytes
-- some gems have assets 
--- can get quick large
- templates like gems same rules
- ownership
-- if answer is yes
--- ie amzn
-- if lf does
--- need right approvals from right legal dept
- does it require AR testing
-- if so then has to go in o3de or o3de-extras atm
-- might be able to expand testing (latest)
- if not doesn't necessarily need to go in there

Nick_L
- we have a remote repo system
- if maker wants to retain ownership without being beholden to outside requirements
- then keep it in your own repo
- if you want to donate to LF
-- see flowchar
-- and fine to be part of AR
-- and want it to appear for everyone
-- then can make sense in extras

colin
- one disagreement, discoverability is not a requirement
- the link is only what's needed for discoverability
- usage should be the same

Nick_L
- if you have a website where folks get your product
- then just as discoverable

colin
- discoverability lists
- taken in by o3de AR
- in the list and can click on them
- once activated you have all the objects ready for you
- is it canonical
-- see earlier in colins e-mail definition
- why we want to fracture the engine a bit into a core and everything else extras
- extras composite repo of canonical repo
-- tested in dev and shipped in release
-- but core engine will build
- tsc has final build on what's core and what's not
- some things that don't fit the defn can be included if the base engine value is diminished without having it
- if folks use it all the time then we could promote it to core
-- tsc decision
-- sigs are front line
-- if code comes in
-- PR
-- new gem
-- PR is for o3de/o3de
-- SIG things this is a core object
-- they can say yes as that's their purview
-- however the tsc could disagree and say put it in extras instead
- tsc more reactive than proactive
- sigs more proactive

- if canonical goes into o3de or extras
- if core goes into o3de main repo

geds-dm
- anything that's canonical goes into the o3de/o3de (?)
-- to be considered canonical it has to be in one or the other
- to be core it must go into the main o3de/o3de repo
- is it up to the sigs to say they don't think it is canonical

colin
- someone could disagree and say something is core
- in which case it should be brought to the tsc for resolution

9p
- can send that out internally
- make a discussion thread about it on the tsc
- so others can give input and feedback
- especially seeing how this meetings attendees low

colin
- sure, this is straight out of my head
- need more ppl to review and say yes/no
- tsc's thoughts won't impact the work
-- can always change it
- it goes into what external repos look like
-- and further into detail
- any questions

geds-dm
- canonical would be up to the sig group to determine in that area of expertise
- whether canonical or core
- core final decision rests with tsc?

colin
- proposal there would be tsc would be reactive
- sigs make decision, if someone disagrees, go to tsc for resolution
-- could be lf or whoever
- none of this is set in stone
- except ownership will be enforced
- if contributed to LF repo then ownership transfers at that point
-- you lose ownership on transfer
- they will change it to a permissive license or will change it

Nick_L
- to do it safely the owner should do it b4 donating it

colin
- if the sig has a big PR with GPL on it
- sig must not accept

nick_L
- correct, as original author has to update the license
- and resubmit or be removed

colin
- word is that you are participating


Nick_L
- should follow the well trodden path with regards to licensing
- original author must make it conform to requirements
- OR if original author can't be found / contacted and it's in doubt
-- then it gets removed

colin
- enabled gems that are  registered will get tested if they have any tests they weill be tested
- if you have an automated json file then it'll assume you want all things tested
- single or composite repoos will be registered and enabled
- as far as AR goes
-- wrote it so that the same AR script can be used
-- if have own jenkins can use the same AR script
-- not every repo has to have their own jenkinsfile
-- other repos can poitn to the o3de repo's jenkinsfile
-- can run jenkins locally

geds-dm
- if going to contribute a gem to o3de, how to get into AR?
- single branch?
- wouldn't want two commits into different repo

colin
- these repos are self contained
- you create the branch of development
- goes through AR
- runs your branch
- yes goes into development
- does the same for o3de / o3de-extras
- make your branch of o3de-extras development
- run the AR on that side
- AR's it against o3de/o3de-extras development
- always what's already in there already that it's testing against
- in the OpenXR stuff, changes have to be paired with changes in the engine
- if they are so highly coupled that they will break
-- you'll likely doing it wrong
-- should re-think what you're doing
-- should be able to indpeendnehly submit to engine first and pass
-- then put changes into the extras and have that pass against development o3de

Nick_L
- alternatively you could pin the version in use
- so that newer ones isn't fetched
- should update engine first
- should work with old version of the gem if possible
- backward compatibility is nice but if it breaks temporarily until new version of gem in
- need to watch out for release schedules
- if going to make it 10 months to make it exactly backward compatible
-- vs. 1 day btweeen commits

colin
- that is the 2nd reason for having the automated json in the extras
- can disable something in extras as they're optional
- eg. XR gems and engine not submittable apart
- can disable testing on the XR object if that's the source of the error
- go to the extras, PR on that
- next PR enable the gem again for testing

geds-dm
- 3 PR workflow
-- go into extras
-- go into main
-- go back to extras to make gem updates and re-enable AR


Nick_L
- would need to make sure this is not done in the middle of a release
- but on development branch
- would have to fit in the development cycle for a given release

colin
- that's the current thinking for that
- util we hit a situation where that doesn't work
- can always do a force on it if required
-- on both and be done
-- extremem case and can't think of a case
-- maybe AR scripts themselves or something

geds-dm
- limitation of changes in the core repo that gems are legacy
- probably should be part of extras

colin
- e-mail talks about what this unblocks
- this unblocks determination of what gems will be getting moved to o3de-extras
- and the ones that cannot be moved into extras, like the aws stuff, should be in an aws repo
- rest of that section was about project manager and what our plans are
-- caveatted that it doesn't quite exist yet
-- discoverability doesn't exist yet
- does a lot more than projects (the project manager)
- tsc should make the final call on some of these things
- large moving of objects


Nick_L
- mcuh as possible delegated to the sigs

colin
- agreed
- initial one 80 gems
- probably going to move 30 of them
- go to the tsc and say 'this is what we're thinking'
- everyone from the sigs can then say yes or no to the list
- then can go into one at a time as they come up

9p
- that sounds good

colin
- came up inanother meeting
- when it goes out it's good for amzn
- need to spread the word inother sigs
- all processes need to be updated to included o3de-extras
- if going to triage need to be not just looking in o3de/o3de but o3de/o3de-extras

9p
- already mentioned in last joint meeting
- can mention again in next joint meeting in 2 weeks
- would be good to know if this is being observed

geds-dm
- 1 issue
- no issues in o3de-extras yet
- not a lot of use yet
- as gems get moved over and issues filed
- then issues will start to come in

colin
- once gems, and any object moves
- will need to do a process to move their issues
- issues should live where the code lives
- get xr issues in o3de/o3de would need to move
- unless it deals with xr code left in main engine
- if there are lots of issues we should proably move them over
- o3de-extras repo has almost the same tags
- didn't copy all
- like wf08, workflows, seemd to specific
- part of the triage is not just whether real or right but if in right repo
- 

geds-dm
- what's the process to transfer an issue from one repo to another
- will original reporter still get notifications?
- wouldn't want an external contributor come in and have it get moved and then not get updates

colin
- could do somethign maybe of closing the issue with the link to the new repo with the new issues

geds-dm
- transfer issue button, can change repo there

colin
- we can test it out
- would be nice to see how fast the core engine builds without all this extra stuff

Nick_L
- spent the last few weeks looking at compiler traces
- object size analysis from clang

colin
- idea of how long gems are taking?

Nick_L
- core framework adds a really large amount of time due to template span
- classes are all reflected, and binded
- each and every call anywhere to the attribute call costs 1.2 seconds
- behaviour bindings
- templates eBus, tempmlates have templates
- lack of type erasure
- at top might be derived from non-templated code
- our tempmlates tend to be safe
- ebus on 2 types
- internally expanded to 4 or 5 types
- core nodes took 15 minutes
- a few seconds of parsing
- rest split into 1/3's
-- 1/3 generating tens of thousands of templating functions
-- 1/3 compiling those functions
-- 1/3 optimization pass on thos tens of thosands of functions
- no magic bullet
- actual templates have to be fixed and cleaned up
- yes we could compile fewer gems
- we can't add 5 min and 20 megabytes to each object file that exists
-- then you could compile 100's of gems
- the gems are slow not because of what the gem does but what the incldued framework does
- all cascades

colin
- trying to get a number to think about
- is it around 30% for gems
- or is it 60%?


geds-dm
- if going to make a discussion topic
- can you attach a link to the topic #57
- as it answers the question that was brought up
- as to the guidance and who makes that decision


9p
- if you put that there we can put that on the agenda for the next sigs/tsc meeting

colin
- was that issue about cross-cutting sig
- mobile

9p
- checked with royal
- concolusion
-- solicit first few items that mobile group wanted to tackle
-- start to work with the existing sigs
- few days ago msg royal, ai on his part to communicate outcome to those folks
- he did confirm that he did or wwas going to do that
- not sure on outcome of that discussion
- all waiting and seeing until response from that convo
- next week office-hours!
