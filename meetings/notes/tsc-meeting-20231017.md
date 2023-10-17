tsc-meeting-20231017.md

# TSC Meeting - 10/17/2023 

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L 
* Geds-dm [Amazon]
* RoddieKieley [Red Hat]
* naomiwash
* Nana Yellen
* Sid Moudgil [Amazon]
* null
* Joe Bryant [Amazon]


## Agenda
https://github.com/o3de/tsc/issues/99

## https://github.com/o3de/tsc/issues/99 - TSC Voting members + SIG Chair discussion

* We need to find the original list of TSC Voting members
* There doesn't appear to be an actual rule about sigs having the same chair across sigs
* We don't want to give the illusion nobody is working on it.
* We could combine discord channels together, even if we don't combine all their repos and stuff
* A larger merger of discording discord channels and potentially sigs
* We would not delete or close sig repos, but we could put a note at the top of the readme for the repo and say its used for historical data.
* TSC deciding which and what channels and sigs should merge - it should be the inactive ones.
* We need to find out why those SIGs came into being in the first place.

Nick L Notes: "We went through each current SIG to see if they are active / code contributing.  
Sigs that definitely should not be merged should be sigs that contribute to code (as well as release, as well as sig-docs).

- Sig-operations has no charter, has no recorded meetings, and is inactive.

Nick L Notes:  We had a discussion about merging sig-core and sig-platform - its potential.  But there's also the mobile working group
which has no sig - so mobile or android issues could bubble into sig-platform.

- We might want to transform to use a sig-mobile instead (re-evalue around february) - in which case we switch sig-platform for sig-mobile.
- restricted platforms would never be part of the LF anyway.
- AR/VR would be under platform - where does it go?  It might go under the graphics/audio sig.
- All the deployment process of AR/VR is like android.  Its all openxr api so it can go thru graphics.
(Naomi taking notes for actual Action Items)
- colinb jumped onto a call with SIG-simluation to discuss triage of items that are flooding in to SIG-Core.  5 pages a week to triage
but most are not for sig-platform, a remaining page and a half (30 issues) for sig-core, at most.  (Some weeks there's less)
- geds-dm:  Making sure that if we merge sigs, that when someone has a platform problem, they have somehwere to go.
- We need more people involved in sig-core.
- Now that we have the monthly calls, perhaps we can use that to help get more sig joiners.

* How do we get the flywheel started and running?

---- Demo of no-code mode ----

Action item:  Schedule onboarding meeting + talk about reducing AP startup time by producing a pre-processed cache, perhaps at least of
materials and shaders and other small files that take a long time to produce (do not need to ship textures)

