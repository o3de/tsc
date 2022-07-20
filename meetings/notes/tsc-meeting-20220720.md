# TSC Meeting 2022-07-20 Notes

## Attendees

- Jeremy Ong
- Karl Berg
- Nick Lawson
- Roddie Kieley
- Royal O'Brien
- Tobias Alexander Franke

- byrcolin
- geds_dm
- tomhh (hultonha)


## [Agenda](https://github.com/o3de/tsc/issues/41)

### [Bug and feature bounty program](https://github.com/o3de/tsc/issues/41#issuecomment-1188404772)

_From user OBWANDO_

- Carry over from last week
- Bug and feature bounty programs have been seen to work elsewhere, in particular around security
  - How much such a program work both technically and procedurally?
  - Could it accelerate our growth for bugs and features?
  - What could we offer as motivation?
- Want to reduce friction to start and ensure first effort success
- Prerequisite would be using the [good-first-issue](https://github.com/o3de/o3de/labels?q=good-first) label as well as the [size/](https://github.com/o3de/o3de/labels?q=size%2F) labels effectively
- Want to avoid cases where bad "fixes" are submitted to cash-in but that introduce other issues
  - Maybe there is point accumulation over many submissions?
  - Could do that as a separate initiative?
- What about recognizing existing contributors doing great work?
  - Maybe through hardware assistance?
- Different types of recognition with short term burst versus longer term affect
- Different types of motivation for particpation; intrinsic "scratching an itch" versus earning a reward
- Focusing on growing the upstream contribution through downstream usage
- Also hands on hackathons and workshops with [O3DCon](https://events.linuxfoundation.org/o3dcon/) are planned
- Feasible to create a cirriculum to focus on the education aspect?
  - Some of that in the works at LF
  - More technical deep dive blog posts could also help here
- Could also look at sponsoring other projects that are meaningful for [O3DE](https://www.o3de.org)
  - The mega grant program that Epic runs has been very successful in this regard
  - There'd be an application to fill and apply with
  - For example the [Open-Asset-Importer-Library](https://github.com/assimp/assimp)
  - Good recognition and giving back for the technical community
    - Gaining visibility through contribution
- *Conclusion*
  - Neat idea but we aren't quite ready for it
  - Also some questions around implementation outstanding


## Emergent Discussion

### Potential for a sig-mobile?

_From user OBWANDO_

- There has been a suggestion for a sig-mobile as distinct from sig-platform
  - If we were to break down sig-platform in that way would we break down sig-platform?
  - Mobile partners are looking for ways to collaborate
- Conceptually would fit a working group better
  - ephemeral concept that can spin up and down
  - is cross-cutting
  - existing mechanism that is a fit
- No immediate action required, but the *recommendation* is to go the working group route

### Participating in other standards bodies 

_From user byrcolin_

- Proposed that we consider joining groups such as [Khronos Group](https://www.khronos.org/) and the [Metaverse Standards Forum](https://metaverse-standards.org)
  - [OpenXR](https://www.khronos.org/openxr/) of interest in particular
  - [Interoperability](https://metaverse-standards.org/news/press-releases/leading-standards-organizations-and-companies-unite-to-drive-open-metaverse-interoperability/) a key focus of the [Metaverse Standards Forum](https://metaverse-standards.org)
  - Legal and IP issues need to be considered
  - A good idea for us to be involved in concrete efforts w.r.t graphics interchange e.g., [USD](https://github.com/PixarAnimationStudios/USD) [glTF](https://www.khronos.org/gltf/)
- Should review the groups mentioned for further discussion
- Ultimately it's people that attend working group and advisory board meetings to help steer direction
- *Conclusion*
  - Should bring this topic up for discussion next week

### Discoverability of partner and contributor projects

_From user byrcolin_

- Starting with external projects/gems
  - Some technical requirements as to how the new json files about the repo would work
  - If we had a public registry, who would have the authority to make changes?
- Likely needs an RFC for community feedback, possibly from within a SIG, and then after a period of time for comments further review by the TSC
- *Action*
  - byrcolin to put something together and bring up as a future actionable agenda item


## Detailed discussion log

Bug and feature bounty program (carry over from last week on behalf of @OBWANDO)

Royal - I've seen bug bounties and feature bounties work in other companies.
  Would like people to think about how a program like this could work. 
  How could it help accelerate our growth for bugs and features?

Roddie - That's a good suggestion to drive some motivation in the community.
  One question is how to set it up technically to make it happen (process, labels, etc.)
  The other question is what is on offer (money, swag)?

Royal - I think people are more likely to continue working on something by helping them over the initial hump

Roddie - Do we as the TSC have ideas on reducing friction that might be outside the reward system?

Nick - We have a lot of bugs that could use fixing but most of them are not suitable first projects.
  Ideally a person's first task is a success.

Royal - We definitely should be using the "good first task" label better

Nick - The other sticking point is how you evaluate the size of a bounty.

Royal - We do have the resources to support it though so we'd want to put it to use.
  Maybe what could work well is the T-shirt size label. Maybe that could work?

Nick - Once cash gets involved though, people lose their minds.
  There will be submissions that "technically fix the bug" but introduce other issues.

byrcolin - The cash shouldn't be on a per-item basis. e.g. there is a point accumulation and more of a winner take all system.

Nick - I'd be wary about making it a competition.

byrcolin - Could do a threshold like 3 points being a tshirt

Royal - We could do that as a separate initiative

Tom - A great example is a user pollend who has done great work and it'd be great to recognize that contribution somehow

byrcolin - Hardware rewards sound great

Roddie - We're talking about something a little bit different though (recognizing people that are doing great work already vs incentivizing new contributors)

Royal - We're looking for more short term accelerants. e.g. capturing a person's free time

Jeremy - I'm a bit more wary about using fiscal incentives to sort of artificially boost community growth.

Roddie - We can focus directly on getting the t-shirt sizes and good first issue labels working well first.

Nick - Yea if we haven't done that, we wouldn't get the bounty program to work.

Royal - The question is what we can do to standardize to get people to contribute.

Jeremy - Ultimately, looking at the projects I've contributed to in the past, I ultimately contributed to scratch an itch, because it was something I needed, not because it was a listed issue as a "good first issue."
  Maybe we could look to do more technical deep dives

Royal - These are all really valid, I want us to explore other avenues. One difference for us is our corporate sponsorship.

Karl - Focusing on growing the upstream contributor space by growing the downstream usage space is a good idea

Roddie - Do we have hands on workshops in the works?

Royal - Yea we're working on that and will be doing some hackathons

byrcolin - is building a course curriculum on using o3de feasible?

Royal - Yea we have some of that in the works via LF

Roddie - What's our conclusion here? There have been some pros and cons discussed, Royal do you have a take or conclusion?

Royal - The conclusion is that it's a neat idea but we aren't quite ready for it and there are questions about implementation
  Didn't come out with an outcome but we learned a bit more.

Jeremy - Using our funds to sponsor more projects we use and write about our usage is another way to get broad phase visibility.

Karl - I'm a fan of the college course approach to grow the community of users as a long term multiplier

Royal - I've been working with some programs to work on some of that to encourage learning past web tech for CS majors

Roddie - I like the thread of recognition for existing contributors and libraries used also

Nick - Many other ways of doing it also (e.g. a tag/role in Discord)

Roddie - Does anyone have final closing thoughts or other ideas while we close off discussion for today?

Royal - There has been a suggestion for a sig-mobile separate from sig-platform. I have two mobile partners interested in that focused discussion

byrcolin - If we do break down targets like that would we break up sig-platform as well.

Jeremy - I would suggest a working group as a more ephemeral concept that we can spin up and down, is cross-cutting, and a more natural mechanism for this sort of thing.

Royal - Yea a working group could live on its own and that could work.

Roddie - Sounds good, no immediate action but this sounds like our recommendation as the TSC on this topic.

Karl - Do we have more details on what these mobile partners are looking for?


