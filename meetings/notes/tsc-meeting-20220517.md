# TSC Meeting 2022-05-17

## Attendees

- Karl Berg
- Roddie Kieley
- Nicholas Lawson
- Royal O'Brien
- Jeremy Ong
- Tobias Alexander Franke

## [Deprecation Policy Discussion](https://github.com/o3de/tsc/issues/30#issuecomment-1126714031)

Feedback was solicited on changes made to the [Deprecation Policy RFC](https://github.com/o3de/sig-release/issues/50) which included
changes/clarifications to the scope (RFC refers to API deprecation specifically), deprecation timing (flexibility added, timing
constraints relaxed for features marked volatile), and refinements in other areas.

It was mentioned that the TSC does not generally "ratify" RFCs as the TSC as a governing body primarily hones the process needed to
actuate decisions, but nonetheless feedback was provided. In general, it was observed that the relaxation of the timing was preferable
relative to a fixed 2-release cycle to permit volatile systems to move quickly. The TSC would help implement any changes needed once
the RFC was ratified.

A comment was made about whether we should strive to deprecate nothing, but counterpoints were made that many systems in the engine
are not yet mature enough to make an aggressive "no deprecation" policy practical. It was also mentioned that the scope of the RFC
should be "what to do when a SIG decides to deprecate something," not "should a SIG deprecate something or not."

## [Election process improvements](https://github.com/o3de/tsc/issues/30#issuecomment-1128966038)

Feedback was offered to request more context on candidates that were nominated or sought election into chair and co-chair positions.
Royal has a draft template for candidate Q&A to be discussed [here](https://github.com/o3de/o3de/discussions/9585).

## [Legacy gem promotion](https://github.com/o3de/tsc/issues/30#issuecomment-1128966724)

A question was asked about whether work was ongoing to promote gems in the legacy Lumberyard 1.x project to O3DE. A point was made that
some of the code was not ported due to license restrictions, and other portions of the code were either dropped due to incompatibility
(e.g. new renderer), replaced (e.g. new navigation and terrain gem), or simply not completed due to time constraints.

From the [list of available gems](https://github.com/aws/lumberyard/tree/master/dev/Gems), a few candidates of possible future ports
included Clouds, Footsteps, Lighting Arcs, Rain, Snow, TouchBending, Water, and RoadsAndRivers (largely graphics feature gems). The
graphics SIG would be a good venue for discussion for porting these.