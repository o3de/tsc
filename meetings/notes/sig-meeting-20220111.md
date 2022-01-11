# TSC meeting - 2022-01-11

## Attendees

* Jeremy Ong
* Royal O'Brien
* Karl Berg
* Nicholas Lawson
* Tobias Alexander Franke
* Sandeep Bisla

[Agenda](https://github.com/o3de/tsc/issues/6)

## [Feature Grid/Roadmap transparency discussion](https://github.com/o3de/o3de/discussions/6703)

KB - If we clone the feature table each release, do we need a dedicated release column
ROB - Status can change/destabilize with future code updates (table is meant to be a living document). Stability doesn't imply correctness.
NL/KB - Should we disambiguate API stability from feature stability
ROB - Each release, the idea is that sig-build will snapshot the table
KB - API, Code as separate columns
ROB - Goal is to glance at the table and identify areas where contributions could be made
(ROB to send messaging out regarding sig subsystem/detail data)
SB - Disambiguate content stability from api stability and functional stability

## [Third Party OSS Dependency Proposal](https://github.com/o3de/tsc/discussions/7)

ROB - Two distinct pieces (legal + technical). This document sets the bar from a legal perspective
NL - People looking to contribute and add a new OSS dep would fill out this questionnaire. Downstream process to either approve or disapprove
(NL to take a shot at drafting technical guidelines for 3p usage)
Preference for fewer as opposed to more
KB - No disagreements
NL - Technical mechanism for inclusion (prebuild binaries and upload to CDN). Could leverage CMake and source distribution
KB - Some libs make sense with source distribution (e.g. ImGUI, single STB-style lib)
JO - Binary size/compile size may be a useful razor for how this is distributed
TAF - What happens when dependencies collide across multiple dependencies
NL - CMake is target based, so this ends up being robust

(circling back to draft NL will draft)
NL - Draft will need feedback from sig-build to enforce
ROB - Do we need a defense mechanism from repos going stale using forks
NL - Depends, but we are exposed if the github is deleted, but it's not in line with OSS principals and maintenance effort

JO - Are there prescriptive restrictions or requirements to licenses we should be aware of?
ROB - Put questions in the thread (there are existing practices regarding copy-left licenses etc.)
NL - Formal process for giving people maintenance privileges for 3p packages (uploading to CDN). Currently it's a heavy process with a lot of validation + testing

## [Request for Comment (RFC) archiving and discovery](https://github.com/o3de/o3de/discussions/6718)

To be discussed at a later date.