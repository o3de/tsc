# Joint TSC : SIG Meeting 2022-05-24

## Attendees

Karl Berg
Nick Lawson
Roddie Kieley
Royal O'Brien
Jeremy Ong

## Agenda

### [O3DE Gem Discussion](https://github.com/o3de/tsc/issues/31#issuecomment-1133084775)

Q: Is there a clear definition of "what should be in the main O3DE repo"?

Ownership is largely community driven, given that the cost of gem inclusion is a cost largely incurred by the community, including:

- Issue triage time
- PR review time
- Cost/time to run tests
- Instability if the gem breaks

Partners always have the ability to host gems and gem building/testing infrastructure externally, licensed however they want, using
whatever mechanism they want. Currently, the process of moving particular gems out of the main repo is predicated on community
feedback, which includes partner feedback (partners are part of the community).

A doc may be proposed in the future to provide further guidance on gem inclusion/exclusion, but for now is decided on a case-by-case basis.

Q: What is the process for migrating code out? What is the process for external gem promotion? What is the process for doc ownership transfer?

Generally, the primary mechanisms for addressing the above is the RFC and PR process with the appropriate SIG or committee (networking, marketing, docs respectively).

### [Cross-SIG Triage process ownership](https://github.com/o3de/tsc/issues/31#issuecomment-1132112577)

Notes courtesy of @forhalle

- It was concluded to not pursue this idea due the difficulty in aligning schedules across multiple entities.
- The TSC was comfortable, however, with leaving this triage to the SIGs themselves (as this is a common pattern for open source projects).
- If we do not find a volunteer to lead this effort, @forhalle will communicate out the impact to SIGs (they need to triage issues with no sig/ labels)
- Regardless, @forhalle will add an item for sig/operations to create a bot to auto-close stale issues (perhaps post emailing a list to sig leads for final consideration), and will indicate critical/blocker issues should be escalated on a more frequent cadence that other issues.

### [SIG process discussion](https://github.com/o3de/tsc/issues/31#issuecomment-1133146843)

Q: What is the process for chair abdication?

The co-chair becomes the interim chair, but a new nomination/election is expected

Q: What happens if an individual chairs multiple SIGs?

An individual is not supposed to chair multiple SIGs, although they can hold a chair and a co-chair position simultaneously. Some relaxation was needed when SIGs were initially formed, and this will be addressed on a case-by-case basis.

Q: What is the SIG chair election frequency?

Yearly.

Suggestion: Discord channel for place for "new contributors" to find places to start and for SIGs to advertise good starter projects.

Suggestion will be taken.

### [Contributor process survey](https://github.com/o3de/tsc/issues/31#issuecomment-1132222954)

Without making any prescriptions on process changes, the TSC would like to solicit feedback from all the SIG community members about the following items:

- Cost of contribution and impact
- Sources of friction (work duplication, AR, compile times, process clarity)

### Miscellaneous

- Royal will be spinning up a new regular meeting to house 5 minute demos to socialize ongoing developments with O3DE.
- TSC will soon hold co-chair and chair elections
- Jeremy OoO next week, Royal to run next meeting
