# TSC meeting - 2022-01-18

## Attendees

ROB - Royal O' Brien
JO - Jeremy Ong
KB - Karl Berg
NL - Nick Lawson
TAF - Tobias Alexander Frank

## [Agenda](https://github.com/o3de/tsc/issues/9)

## [Splitting Sigs](https://github.com/o3de/tsc/issues/9#issuecomment-1015517476)

ROB - Need a charter so that TSC understands the impact of the Sig proposal/change
THH - OK we'll emulate other existing examples. How do we evangelize the charter
ROB - That'd come back to the TSC, remember to modify the existing charters for sigs that are affected
THH - Logistically, where should the draft charters go?
ROB - Discussion thread in markdown works

## 3p license clarification

ROB - To clarify with Scott any license shrinkwrap considerations

## Deprecation policy discussion

THH - Deprecation policy originally adapted from Amazon's internally policy. Goal is to minimize downstream customer impact. Encompasses not just software/feature stability, but API stability as well. This doc presents a runbook of steps we can follow, caveats being that the process is a bit heavy, and there is a manual step needed to remove deprecated APIs in subsequent releases. This process could be something that docs/release teams manage. 3 stage deprecation process. There was a distinction internally between wider-scale feature deprecation, and finer-grained deprecation.
JO - Should the deprecation policy proposed apply primarily to systems we believe are stable
THH - This could be a wider discussion, but we could define the point at which a system needs to annotate deprecation at this granularity
ROB - We need to define the checkpoints for when state transitions occur or we risk the operational maintenance being lost in the process (we would like a formal timeline)
THH - Have to jump, but can catch up and refine the proposal for the next weekend
ROB - Notification model for the sigs as well

## Feature grid

ROB - Column suggests are good but would not look good under GH markdown formatting.
JO - Suggest that we specify data as metadata in a JSON file (backed by a JSON schema) which we can then use to populate a table rendered in Hugo on our docs page
ROB - Agrees
(JO to propose this in a future meeting)

## Emergent topics

ROB - TSC should solicit feedback about what would be proposed for the next release
JO - What's the best way to communicate with all the chairs?
ROB - We should make sure the mailing list is working (action item: to form o3de-chairs mailing list)
(JO to later communicate to chairs regarding feature grid + future release intentions)
TAF - Android support doesn't naturally fit well into the table given its cross-cutting nature
ROB - Sig-platform is the cross-cutting sig which would then disseminate responsibilities across to garner support. Driving it is on the onus of the proposer
TAF - (offers example of how Android support may be specifically lacking in a particular category e.g. file streaming)
ROB - Proposal would go to individual working group/sig to address specific line items. TSC can spin up ephemeral working groups to address these issues
TAF - Any news on new members to the foundation?
ROB - Yes but no. But yes.
TAF - Another question, are there any considerations regarding telemetry?
ROB - Under active discussion, with a number of considerations. Data could possibly flow through LF, would require user agreements, etc.
ROB - Coming up, we'll be surveying projects being worked on by partners for TSC to get appraised on and get sigs involved in. LFX security will be providing a security suite to start scanning repos and highlighting potential vulnerabilities (e.g. [link](https://security.lfx.linuxfoundation.org/#/a09410000182dD2AAI/foundation-details))
