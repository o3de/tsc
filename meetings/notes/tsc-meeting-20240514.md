# TSC Meeting - 5/14/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* jjsteele [Bay Software]
* lemonade-dm
* Luis Sempe
* Naomi Washington[LF]
* Nick_L
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]


## Agenda items
https://github.com/o3de/tsc/issues/124

### Agenda Item: Ad-hoc - Nick L Stabilization Branch is cut

### Agenda Item: Ad-hoc - Naomi Washington [LF]
* Regarding the roadmap, how do we direct people to things that we want them to work on that applies to the roadmap?
* My reaction was to go point them directly at github, they end up at o3de.org/roadmap - get them to the short list quickly.
* I would like to add a tag to the issues
* Nick:  The project roadmap items have no tags and are not issues.
* Nick:  We should have a CTA and a "next step" on where 

* APMG is getting console licenses for middleware to get console platforms supported.
* Luis - Crucible assets?
* https://overlo3de.com

* Colin: If I keep having to make the changes to the 1.0 template / manifest then its a long and difficult process
* Whats the incompatibilities between 1.0 and 2.0 ?
   * Colin:  Versioning is good but assumes zip files only.  I'll be adding source control (github/gitlab/etc)
   * All the objects become non portable due to the structure since its all stuck in the parent.
   * Duplicates data.  It violates oop, theres a lot of problems.  Lots of fairly poor decisions that are removed for 2.0 but have to remain in 1.0 for legacy support.
   * (Discussion about technical details about repos and stuff).
   * Colin: When you add the link to the repo to the manifest, whenever there's a change (Talked to Mike C about this) to the root objects json, on commit theres supposed to be a github action that automatically copies that repo.json to the static site.  (canonical.o3de.org) so the program manager can download it.  Whats ACTUALLY been happening is htat people have been editing the o3de.org repo json, instead of the json inside the repo.  So they have been editing it on the website.  Mike is aware of that and is looking at how to get it to work.
* More formalized in 2.0 is a license section.  Those licenses (for example, 3 different licenses, MIT license, Apache-2.0 licenses)
* Lots of other changes need to be done for a 2.0

* Thinking we do a couple versions before we do 2.0.  Maybe 1.1 and 1.2 and 1.3 to make steady changes.  Maybe 2.0 is not needed because it would imply that its completely different.

