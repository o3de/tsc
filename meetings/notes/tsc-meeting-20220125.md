# TSC meeting - 2022-01-25

## Attendees

* Royal O' Brien
* Jeremy Ong
* Karl Berg
* Nick Lawson
* Tobias Alexander Frank

## Non-TSC Attendees

* David Greer
* Tom Hulton-Harrop
* Aaron Ruiz Mora
* Pip Potter

## [Agenda](https://github.com/o3de/tsc/issues/9)

## Feature grid, JSON schema feedback ([link](https://github.com/o3de/o3de/discussions/6703#discussioncomment-2043989))

JO presented initial stab at the JSON-based document to outline subsystem/feature stability.

Feedback provided:
- Consider how the docs would need to be updated when a new platform is introduced
- Consider how the JSON doc would be authored (previewing/editing tool would be appreciated)
- Consider alternative ways to organize the doc if the doc size is too large after the initial pass
- Consider where it would be stored (consensus is that it should belong in the main repo so that PRs can atomically amend the feature grid docs)

## [Sig-simulation](https://github.com/o3de/tsc/issues/10#issuecomment-1021128991)

Discussed doc with general consensus that sig-simulation formation made sense

Feedback provided:
- Consider keeping AZStd/math facilities in sig-core
- Consider separating specific feature implementations (e.g. NvBlast) in a separate section so that the "scope" encompasses alternative hypothetical future implementations
- Consider fleshing out the sig-simulation goals (and include detail about what constitutes a "sig-simulation" concern, e.g. time-dependence, modeling some physical behavior, etc.)

JO to solicit additional buy-in for sig-simulation formation from other TSC members while sig-core and sig-content chairs/members continue to iterate on draft.

## Miscellaneous

Tobias raises an issue of duplicating work and mechanisms to ensure development efforts are duplicated (Example offered here was DDGI probe visualization)
Response: Existing sig triage meetings + GitHub issues should be the primary defence against this