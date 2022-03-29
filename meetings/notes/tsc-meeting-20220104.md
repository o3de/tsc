# TSC meeting - 2022-01-05

**Facilitator:** Jeremy Ong
**Notes taker:** Jeremy Ong

## Attendees

* Jeremy Ong
* Royal O'Brien
* Karl Berg
* Nicholas Lawson
* Tobias Alexander Franke
* Pip Potter

[Agenda](https://github.com/o3de/tsc/issues/5)

## New sig-testing label request for `FixVerified`

[Item link](https://github.com/o3de/tsc/issues/5#issuecomment-1004930074)

* `Broganab` was unable to connect to the voice call unfortunately so the original presenter wasn't able to attend.
* Concern raised was that there are already labels that seem possibly useful for the intended purpose, and having more unused labels makes the issue tracker more difficult to use
* Agreement that TSC would assist if this had global process implications

### Open questions

* Could existing labels be better suited to accomplish this already?

### Action items

* Discussion to continue in [this issue](https://github.com/o3de/o3de/issues/6529)

## Cross-sig approval process

[Item link](https://github.com/o3de/tsc/issues/5#issuecomment-1004346347)

* Sig-network is proposing a new RFC that involves both sig-network and sig-build - question about how the approval process should go
* Generally, sig chairs should coordinate to ensure relevant representatives appear at sig meetings to propose and approve cross-cutting RFCs
* TSC isn't an approval body to approve RFCs, but if a working group is needed to resolve issues that are cross-cutting, sig chairs/members can request a WG be formed and the TSC can form it
* TSC open to feedback related to process issues however

## Vulnerability reporting process

[Item link](https://github.com/o3de/tsc/issues/5#issuecomment-1004346347)

* Sig-security would like to set up a security reporting process, but appears there is some LF involvement needed
* Need a process in place for hosting new projects if not already set up
* Royal to help define a process and consult LF and bring a new-project standup proposal to a future TSC meeting

## RFC archiving/indexing process

[Item link](https://github.com/o3de/tsc/issues/5#issuecomment-1004346347)

* Consensus that we need a better mechanism for discovering and referencing RFCs in-flight or approved
* Currently, RFCs are fragmented across different repos, and it's difficult to determine where to submit/find specific items, or cross-reference RFCs when authoring a new RFC
* Ideally, all RFCs are discoverable/indexed, but in a manner that doesn't require an assigned individual to do any manual collation
* Will take this offline to field different options/proposals

## 3rd-party package approval

[Item link](https://github.com/o3de/tsc/issues/5)

* No formal process currently exists for approving 3rd-party packages/software to be used in O3DE
* Suggestion that an existing sig could be designated to resolve the process once defined
* Royal to coordinate with LF to come up with initial legal constraints for a future proposal
* Nicholas to open a thread to discuss technical aspects of the approval process (independent of the legal license/patent concerns)

## Feature grid

[Item link](https://github.com/o3de/tsc/issues/5#issuecomment-1004935543)

* Would like a feature grid that provides transparency about the engine's systems/subsystems and their state of maturity
* Parallel suggestion to spawn working groups to also make demo content to showcase actual functionality as a better litmus test of capability
* Concern that a living document shouldn't be too granular or it risks becoming stale and subsequently less useful
* Concern also that code completeness/maturity is fairly subjective
* Jeremy to create an issue thread proposing an initial template to give to sig chairs for their sigs to provide
