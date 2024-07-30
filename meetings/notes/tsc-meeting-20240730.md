# TSC Meeting - 07/30/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Adam Dabrowski
* colinb[APMG]
* Jan Hanca [Robotec.AI]
* JT [SCB_GameDesign]
* Luis Sempé
* Michał Pełka [Robotec.Ai]
* Naomi Washington [LF]
* nick_l
* null
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Agenda items (official)
Agenda Topic: https://github.com/o3de/tsc/issues/134

(No topics logged)

## Announcements / Topics to discuss while everyone is here

### Announcement/Topic - colinb - current status
* colinb:  worked on adding a 'discovery' page for the remote repos page in the Project Manager
* Click "Engines" -> "Remote Repos" as per usual.  You can type in URL and add the gems to all the gems available.
* Discoverabily is the problem there - who knows what sites are available.  I put through 2 seconds (list boxes).
* One list box is named "partner repos"
* One list is called Community Repos
* I propose that anyone link things in the community repos.  It can be a very low bar, it must work, it must show their objects, do something correct.  No other guarantees.  
* O3DE does not vet the contents of the repos.
* The difference between them is that the partner repos have a higher bar.  They have to work, they should not include objectionable material, etc.  The standard there would be legality, and is from a known trusted source such as a known contributor / maintainer / etc.  If there's an objection to anything in there, the person who contributes that repo has some time limit to remove or is demoted.
* The idea is that everyone to list whatever they want there, in lieu of a search engine.  Friendly and open to the community so that people feel free to post whatever creations they have there.
* One thing I wanted to discuss was how that process works.  I still think we do it via pull request.  If its a core repo, release cadence.  If not, its a file on the webserver or something like that. Kind of what I was thinking.  More dynamic for people.  Content would change dynamically then.
* JT [SCB_GameDesign] - UI/UX they should have quite a bit about this (Maybe look in the UI/UX discord?)
* Trust and Security - should O3DE do trust of remote repos / should we have some sort of 3rd party Organization / do we allow the people to own the repos do the trust.

### Question (Colinb) - Non-free objects?
* (A discussion about mixing non-free objects with free objects in the project manager)

* One option would be that the project manager has a list of app stores, free clickable objects, partners, etc
* That list can come from a dynamically updatable data file, which has its own process for updating/managing, eg, a github site, with its own CONTRIBUTING.md or GOVERNANCE.md and so on.
* Then we could add a URI handler to project manager to accept o3de://repo/ uris.
* USer path would be
   * User opens PM
   * User goes to the "get more shiny stuff" page (Whatever thats called)
   * User sees a list of gettable repos, but also, clickable asset stores and partners
   * User goes to partner website by clickable link
   * Partner website does WHATEVER
      * PopcornFX for example might just have a blurb about their O3DE based solution and then have a clickable link like o3de://popcornfx.com/repos/demo
      * A real asset store might have shopping cart with user management, purchases, etc.  Individual or account purchases would show up and they could click for example o3de://overlo3de.com/purcharses/{SOME UUID TIED TO USER}
         * The real asset store could choose what happens.  Perhaps thats a repo per item.  Perhaps that is a fake repo that actually updates its repo.json dynamically based on what the user has already purchased so that new stuff just Shows Up if we update repo.json for that.
   * Project manager picks up a o3de://url link and adds it to the repos, which causes it to fetch and repopulate the various lists of objects available from that repo.

