# TSC Meeting - 4/23/2024


## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Danilo [Amazon]
* Jan Hanca [Robotec.AI]
* jjsteele [Bay Software]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* lemondade_dm
* luis sempe
* Michal Pelka
* naomiwash_lf
* Nick_L
* null [meta]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Agenda items (Ad hoc) 

### Joe - Release
* Still working on the release notes, lots coming in at the last moment for the point release / actual release
* Google doc is release notes
* May 1st is cutoff date for the actual release

### Joe - Game Jam Success
* A team was able to make a small FPS in O3DE in just one jam.  Which is great progress.
* Windows and Linux

### Joe - Carbonated is having 2 issues with their game
* It takes them overnight to process all their assets
* Perhaps an asset cache server?  Compatible with git/timestamps?
* Have to go thru and make sure they're reprocessing assets which don't need to be reprocessed.
* It appears that the asset processor will sometimes reprocess most of your assets when you make 1 change.  Needs to investigate.
* Joe:  Really press for someone to work on the cache server.  It relies on timestamps (Investigate this?)
* Sid_Moudgil:  Reprocessing / processing.
* Related to AP, the asset processor first time startup experience.
(a Discussion about optimizing the asset browser)
* jjsteele [Bay Software] and nick_l will have a discussion about it, since they are actively working on it.

### Joe - Vision for 2024
* We are trying to reorg our maintainers into a heirarchy and gain a lead maintainer.
* We are trying to figure out our roadmap and vision post september 2024 (after next release)
* We need contributors to help with this.  We can set up a session in the TSC meeting?
* Nick: End of month meeting for TSC can be the vision meeting.

* Joe:  Vision - much better engine for all sizes of projects
* Joe:  Vision - items that we want to propose will be next week - can we implement a UI for exporting projects?
* Joe:  I'm a fan of ship early and ship often.  I am A-Ok to put stuff in phases, it does not have to be perfect.

### Joe - Prioritizing fixing O3DE Extras
* If we have to temporarily remove O3DE-Extras from AR, we are okay, priority is working on fixing it.
* Please don't keep running AR.  Its blowing up our infrastructure costs.
* Ping someone on discord - or Mike, or maintainers, we can help you through it.
* Ping Mike about it.  We need to fix it.  We are moving AR to github actions.  It won't be a cost aspect then, but there's still the frustration aspect.  We suspect it will be more reliable too.git
* Jenkins runs out of memory and disk space

### Colinb[APMG] overlo3de.com has upgrades
* 9 things up now!
* more upgrades to the preview, including repo structure
* status is improving
* Main issues would be getting a page working in the project manager that shows a list of links like overl0de.com
* submitting the RFC coming soon for changes to the project manager.
* Change I was suggesting was an uncurated/curated list.
* (A discussion of overlo3de.com)

