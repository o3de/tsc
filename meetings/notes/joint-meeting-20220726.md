# Joint TSC : SIG Meeting 2022-04-26

## TSC Attendees

- Karl Berg
- Nick Lawson
- Roddie Kieley
- Royal O'Brien
- Jeremy Ong
- Tobias Alexander Franke

## SIG Chairs/Co-Chairs, Marketing Attendees

- byrcolin
- geds-gm
- Joshua Rainbolt
- Yuyi Hsu
- Mike Chang
- Joe Bryant
- stramer


## [Agenda](https://github.com/o3de/tsc/issues/42)

### SIG Updates

- SIG-Platform is working to extend the O3DE object system and hoist non-core gems out of the canonical repo
- SIG-Core is working on improving the allocator linkage model and a new archiving system.
- SIG-Release is holding ongoing co-chair elections and accepting nominations while working on the October release and formalizing the release manager and co-manager roles to ensure future releases are repeatable by the community. SIG-Release is also continuing to develop the roadmap for upcoming releases.
- SIG-UI/UX is iterating on a new process to streamline community contributions and requests (proposed intake process discussed later this meeting)
- SIG-Build is collaborating with SIG-Platform to define how external gems are managed and stored. In addition, the SIG is continuing to iterate on the 3P contribution and approval process. VS 2022 support is discussed later in this meeting.
- Marketing is working on a Twitch channel, podcast series, blogs, and a number of other materials. Marketing reminds the community that the Call for Proposals for O3DECon this October is still open and requests submissions.
- SIG-Networking is working to migrate AWS code to an external gem and has RFCs active for this effort and remote tooling stability and connection improvements.
- SIG-Security is working to refine the SLA policy around responses to known vulnerabilities.
- SIG-Graphics is mainly focused on the material canvas effort, which enables visual-scripting workflows for authoring materials. An outstanding problem the SIG is working to address are asset import problems related to animation, although there is some ambiguity about whether the issue belongs with SIG-Content, SIG-Simulation, or SIG-Graphics

Updates from SIG-Simulation and SIG-Content pending.

### SIG-Assets proposal

- Joe Bryant has proposed the formation of a new "SIG-Assets" group [here](https://github.com/o3de/tsc/issues/42)
- Premise is to have a group dedicated to managing asset license approvals, storage/management, and development of demo content.
- (Jeremy: Perhaps sig-demo might help disambiguate it from sig-content?) Naming feedback is welcome
- (Colin) There's some confusion around the delineation between sig-assets and sig-content responsibilities
- (Mike) SIG is decidedly cross-cutting, if it would be formed with some responsibilities possibly overlapping SIG-Build
- (Jeremy) Is that who owns the LFS systems at the moment?
- (Mike) Yes
- (Joe) There is a large body of assets from Lumberyard we'd like to migrate but need people and mechanisms to ensure license restrictions are honored. Another facet is working with the community on demos and game gems, and working with the docs SIG to publish tutorial content.
- (Pip) Should this be a working group tied with SIG-Release?
- (Joe) Release responsibilities are quite different and the SIG-Release charter is already quite big. In discussions with Royal, the responsibilties in the proposed SIG-Assets charter don't overlap cleanly with other SIGs.
- (Jeremy) Propose a 2-week period for people to read, comment, and offer feedback and will discuss at the TSC meeting August 9
- (JT) Welcomes efforts that expand content that bridges outreach efforts

### SIG-UI-UX [Intake Process](https://github.com/o3de/sig-ui-ux/blob/main/governance/UX%20Intake%20Process.md)

- Discussed iterations to the way SIG-UI-UX processes SIG work and approval processes.
- (Yuyi) SIG-UI-UX is heavily bottlenecked and has a lot of requests to service with varying degrees of urgency from the community and other SIGs. The proposed process includes a GHI workflow, office hours, and other elements to manage the request pipeline and set response expectations. Urgent matters can be brought up at the office hours.
- (Nick) Initial thoughts are that the process reads too "corporate" and imposes too many hard requirements on open source contributors. For example, the office hours aren't globally inclusive. Suggest relaxing requirements and embracing a more asynchronous workflow.
- (Yuyi) Intention isn't to exclude people from contributing, but we need a process to vet proposals and ensure guidelines are followed.
- (Nick) Right but it still reads like there are a lot of hoops to jump through.
- (Jeremy) The "2 sprint/4 week" SLA response time jumped out to me. As a paid contributor, adhering to this might be possible, but in the open source context, even the notion of a "sprint" doesn't exist. There are useful elements here with respect to the GHI flow and other aspects, but would prefer a more "process-neutral" set of guidelines.
- (Yuyi) So to confirm, the general idea is right but ultimately comes off too corporate?
- (Jeremy) Suggest imagining being in the shoes of a member of the community who wants to contribute in a UI/UX capacity as a side passion project. Being an active contributor shouldn't necessitate showing up to a particular meeting on a day of the week, or honoring a 2 sprint SLA. We should try to lower barriers to entry for community members that want to be active.
- (Nick) This project likely isn't going to succeed off a small number of people doing the majority of the heavy lifting.
- (Yuyi) Generally, the SIG receives 2 types of requests: proposed solutions and feature requests. A lot of time is needed to collaborate with ticket owners and iterate.
- (Nick) Agree with ninepoints (Jeremy) here, we should iterate on the process to capture the population of unknown UI/UX experts that may want to contribute. Suggest a wording oriented around guiding contributors to answers to questions like "how can I help" or "how can I ask for help"
- (Roddie) Suggest reframing as a set of "guidelines" rather than a process which implies a more rigid set of engagement rules.

### SIG-Build [VS2022 Support](https://github.com/o3de/tsc/issues/43#issuecomment-1194442290)

- Discussed whether to support VS2022 and how to go about doing it
- (Mike) Community demand for VS2022 is high and there's an open question about how to support and and implications to AR. Would like to seek feedback on timing and impact.
- (Jeremy) Can you clarify if what is meant is the IDE or the toolset? (VS2022 can compile with toolsets older than v143)
- (Mike) Both the generator and the toolset, but the generator also requires CMake 3.21. The issue is if upgrading stipulates that AR times double.
- (Jeremy) We definitely want to lower the overhead of contributing, not raise it, as well as support either generator and toolset.
- (byrcolin) Suggest supporting latest and the previous version, to also accommodate platforms that aren't supported on the current one
- (Joe) +1 for supporting the previous as well
- (geds-dm) Project manager would need to be updated since it forces the 2019 generator at the moment (Joe: yes this would be changed once we decide to migrate)
- (Karl) Cautions against aggressive compiler changes which can impose a lot of friction in the project
- (Royal) We should support 2022 at least and try to maintain 2019 compatibility
- (Mike) Consensus seems to be that we should try to support both but there are still questions about AR costs, can we test both?
- (Jeremy) Doesn't sound feasible to run both
- (Joe) Suggests running nightly builds on the older toolset
- (geds-dm) Another option is to compile each configuration with different toolsets (Jeremy: We'll likely be exposed to regressions still)
- (Joe) Suggest an RFC
- (Jeremy) Another option to consider if we write an RFC is relaxing some warning requirements which are actually the sticking point for why the code isn't immediately forwards compatible with v143. Warning policies tend to break with higher frequency when doing compiler/toolchain changes than actual code which tends to be forwards compatible.
- (Mike) Will write an RFC taking into account the feedback today

### Emergent

- (Royal) Got the SoLoud OSS audio solution working and will push it as a gem
- (Jeremy) Reminder to issue submissions for the O3DECon CFP
- (Royal) Oppo mobile joined as a partner, wants to form a working group to push mobile platform improvements
- (Joe) Clarifies that WGs aren't persistent like SIGs (hence why the SIG-Assets proposal was not made as a WG)