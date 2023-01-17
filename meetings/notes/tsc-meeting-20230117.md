# TSC Meeting - 1/17/2023 - Office Hours

### Note:
* 2nd last of month is office hours
* last of month is Joint SIG meetings

## Attendees
* byrcolin[amazon]
* channele[amazon]
* geds-dm[amazon]
* kberg[amazon]
* nick_l[amazon]
* RoddieKieley [RedHat]
* Royal OBrein [LF]
* Tobias Alexander Franke [Huawei]

## Agenda Items
* Ratification of TSC chair
    * Chair - Nick L [amazon]
    * Co-chair - Tobias Alexander Franke [Huawei] 
* Open discussion

###  Topic: Discussion about the proposal to include a roadmap blurb at the beginning of joint TSC meetings starting end of feb.  Its not a MUST but a can do.
  - Colin suggested the Project board
  - Nick suggested the wiki
  (TSC members did a quick check of the wiki, live, but it throws away work if multiple people work at the same time)
  - Royal suggests just doing a topic issue with comments from the sigs.
(No real conclusion but the topic issue seems to resonate the most with the TSC, as it can be added on the project board too.  Further discussion is possible as this has a few weeks to decid)

### Topic: Colin talking about O3DE Extras
  - Question was whether the other ones (Multiplayer-sample, Netsoaktest, etc) are "Canonical" and part of the release
  - There was no confirmation one way or the other whether these were "Canonical" but they dont' currently appear to be.
    * Karl: mentioned that we need a razor to specify what goes into core + extras.  We've created o3de + grab bag of extras.  We might have to put some thought into subdividing into the customer experiences.  
    * Colin: Added a script to AR that lets it get other repos and enable whatever gems, etc.
    * Royal:  Many other foundations have a lot of repos, and they templatize it.
            What should happen is having a simple readme or markdown list.  Same grid tool could be used to show the stability.
    
    * NickL Asked about whether partial repos can be pulled.  Colin: Technically yes but not in practice
    * Colin indicated that this was the original idea, but its not clear if this was implemented in that way.   Maybe there's a way to do it with submodules in order to get individual pieces?  Perhaps with a release?  the original thought was to have each module individual
    * TSC members don't like the idea of submodules
    * Royal: O3DE being a core distribution - should be thought of that way, where its not littered with unnecessary pieces.  
    * Royal:  Synology can do it?  (Research Synology.)
    (no real conclusion, but further discussion halted so that Chanelle can bring up a topic)

### Topic: Chanelle [Amazon] - Figuring out which repositories can have their documentation in the official o3de documentation
  * Chanelle "I'm looking for feedback on an RFC that clarifies when docs about non-canonical projects and Gems may be included in O3DE Documentation."
    https://github.com/o3de/sig-docs-community/pull/93/files
  - For example, owners should host the documentation if they're not owned by the O3DF or part of the o3de org.
 - Discoverability of features/partners.  
    - Nick L:  Could use the o3de scripts to at least build their doc pages
    - Colin:  Each gem has a doc link.
    - Nick L:  At the most, we should just link to them.  We could keep a list of official ones and scan the repo/gem.jsons.  The project manager should show the doc link for any gem.
    - Royal suggests a strategy where we fork and ingest, so that it stays working even if they destroy their docs.
    - Nick L:  These partners own the gems themselves, so they could destroy the gems as well as the docs anyway
    - Colin: Agree.
    (Ultimately, Chanelle requests that we ciew the RFC (link above) and comment on it so that the Docs SIG can understand what constraints the TSC might apply)
    (Ran out of time here)


