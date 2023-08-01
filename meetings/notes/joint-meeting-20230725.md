# Joint TSC : SIG Meeting 7/25/2023

# Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]
* colinb[APMG]
* drakeredwind01 [Cyber-sec, idea]
* geds-dm [Amazon]
* Joshua Rainbolt [Amazon]
* JT [SCB_GameDesign]
* null [Amazon]
* RoddieKieley [Red Hat]
* Naomiwash
* Yuyi [Amazon]
* Nicole Huesman [LF]
* Nicolas [Red Hat]
* Highfly [Fly Forge]
* Vincentvincent

## Attendees (by discord name)
* Nick_L

## Overall outline
This is an overall outline of the meeting, a full recording is available.
https://drive.google.com/file/d/15tU4yJVFssn60lYwKT2dyQHxHw8QMWzz/view?usp=drive_link

### Ad-hoc topics

## All-sigs reporting in:
See the below link for the topics for discussion this week and information from the SIGs
https://github.com/o3de/tsc/issues/89

### Sig-Release
SIG Release updates can be read here:
https://github.com/o3de/sig-release/issues/215

Discussion:
Release manager and QA is no longer present.  We have to figure out how to fill that QA gap.

### Sig-Core
Here is the Roadmap for SIG-Core: https://github.com/orgs/o3de/projects/31/views/1
* Build fixes were added to support the newest GCC 13/Clang 14 Compilers
* Project Export Scripts for both Engine-centric and Project-centric workflows have been introduced.
* SIG-Core Roadmap: https://github.com/orgs/o3de/projects/31

### Sig-UX
Announcement of the Rev the engine results. Document - https://docs.google.com/document/d/1J6uzkGa9_g3a8AFuN4XnfHeS_uluAPnSMsrCjjbNOS4/edit

This document lists the overarching broad details but there are about 150-200 actual UX issues, which need to be detailed, such as UX design, diagramming, braingstorming, etc, to turn into tickets.

## Action items
* Review https://docs.google.com/document/d/1J6uzkGa9_g3a8AFuN4XnfHeS_uluAPnSMsrCjjbNOS4/edit

## General Discussion
* Naomiwash:  Back to the release discussion.  (Do we do a time based release, or a feature based release?)
* We are targetting a time-based release, (ROSCON), currently, so a feature-based release is difficult to justify.
* JT [SCB_GameDesign] discussed a balanced release that would require a full time micromanaged release.
* Nick L discussed a hybrid approach where you choose a fuzzy date and try to hit it with enough wiggle room to push it out a little bit.  Then SIGs decide to announce what features they expect to have done by then.
* JT mentioned OpenVDB hybrid model, which is similar - they will hit a quarter, for example, not necessarily a date.
* Joshua Rainbolt: If I had to do this, I'd look at the tickets that have been resolved, since the last cutoff at may.
* What about an Eye Candy type tag? Something visual that you can see?  
* NickL "Interesting to release?  Worthy of release note mention?"
* Joshua recommended not to rely on tags entirely, but comb the the tickets as well.

