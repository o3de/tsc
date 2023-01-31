# Joint TSC : SIG Meeting 1/31/2023

## TSC Chair and Co-Chair

## Attendees (by discord name)
- byrcolin [Amazon]
- Chanelle [Amazon]
- Danillo [Amazon]
- dg211 [Amazon]
- dshmz
- geds-dm [Amazon]
- Kadino [Amazon]
- KBerg [Amazon]
- Mike Chang [Amazon]
- Nick_L[amazon] 
- RoddieKieley [RedHat]
- Royal OBrien [LF]
- SergeyP [Amazon]
- Tobias Alexander Franke [Huawei]
- TonyB [Amazon]
- vincentvincent

## General Updates and Announcements

Issue link for roadmap items:
https://github.com/o3de/tsc/issues/64

## SIG updates

### Networking - presented by kberg, for pip
- roadmap: https://github.com/o3de/tsc/issues/64 
- updates  on the client server split
- Multiplayer Sample going public soon - https://github.com/orgs/o3de/projects/22 is the roadmap
#### Questions for networking
- Royal: Does the multiplayer sample have the client/server build seperation?
- kberg:  Everything in the engine does, there is a client, server, and unified.  This is already in developer.
- Royal: Is it in the docs?  
- KBerg:  I believe its been updated.
- Nick_L: Reminder that a build server builds the 'development' docs constantly https://development--o3deorg.netlify.app/docs/

### Testing - presented by Kadino
- for SIG-testing, roadmap link at https://github.com/orgs/o3de/projects/35/views/1?visibleFields=%5B%22Title%22%2C%22Assignees%22%5D
- Public metrics, including working around the Linux Foundations Insights tool which was insufficient for uploading builds.
- Making it easier to test ingame.
- Couple other things to mention, sig build will get into static analysis, which sig-testing intends to support.
- Likely upcoming changes to the build pipeline, keeping the lights on effort.  Want to keep testing as efficient as possible.

### Build - presented by Mike Chang
- Roadmap link: https://github.com/orgs/o3de/projects/39/views/1 
-  We have some impact in our contribution workflow.
- We're looking into any hosted infrastructure on the LF side to augment automated testing or reviews. 
- We're getting ready to issue a proposal for 3rd party package contribution workflow.
- We're looking into static code analysis in github actions.  Already existing structures for it on github, with CodeQL.  How feasable is it to run the builds within and do the scanning alongside with the resources they provide, which are pretty small
- We're working with the release team on whether we can support doing publishing packaes on os-specific stores.  First task is whether we can publish onto the ubuntu snap store.  Investigating requirements.

#### Questions for Build
- byrcolin : Why different CI/CD system.  Cost, flexibility?
- Mike: Both!
- dshmz: Confirmation - failure rate / AR redesign is already available.   https://github.com/o3de/sig-build/issues/77
- byrcolin  : Is this a duplication of existing features or will there be additional ones?
- Mike:  trying to replicate as much as possible, but there are costs on their own, as a suggestion, if we were to move it to github actions.   others could run AR in their own forks for example.
- Nick:  So if they fork the repo they get the AR infra on their side.  Is there a resource limit?
- Mike:  They limit the resources.  2 cores, 3 cores.  Mac windows and linux.

### Simulation - presented by dg211
- roadmap: https://github.com/orgs/o3de/projects/23
- focus is probably more on robotics than what is shown here.  From the meetings I've attended from the sig-simulation governance, the sig goals are well aligned with what Amazon is interested in doing.  
- Robotics is going to be a strong focus this year.

### Release
- Roadmap at https://github.com/orgs/o3de/projects/29/views/1
- Documenting the stabilization and release process.
- Figuring out how we keep the roadmap up to date across the project.
- Vincent's been working with the sigs to get the roadmap issue templates set up, and all the roadmaps we're seeing today is a result of the 
project.  
- I want to thank everyone coming today with those roadmaps.  Its really good to see the work that's in progress.  This is super
good to see and great for the project and to have this visibility.  

- Next:  Work on documenting the stabilization process, the exception process during stabilization - diving deeper, etc. 
- Next:  the point release process, we want to make sure we have docs in place for it.
- The other thing that's going on is a discussion going on about figuring out which repos belong in a release.
- https://github.com/o3de/sig-release/discussions/129 A fairly new repo, considered canonical repository, what is the criteria for including repos in a release.  Please comment on this discussion

### Core - presented by geds-dm
 - roadmap at https://github.com/orgs/o3de/projects/31
- gems and 3rd party plugins can specify a specific version of the gem or project, it should help 3rd party providers like popcornfx get their
ai not be broken by engine updates.
- improving build time performance in core libraries, investigating AzCore, AzFrameworks
- backlog items:  UI Editor for the Settings registry.  Backend is there, but we are waiting on resources for the actual in-editor workflow
- General performance improvements around json-merge format.
- New election coming up february.

### Platform - presented by byrcolin 
https://github.com/orgs/o3de/projects/20
-  : Arm64 support.
- seeing what it would take to support officially redhat as a linux platform
- bugfixes on the different platforms.

### Docs/Community - presented by Chanelle 
- roadmap https://github.com/orgs/o3de/projects/15
- currently Establishing roadmap and items.
- cleaning the backlog for o3de.org - making sure things have the right labels and so on
- having our own project board to track some of the things where there are gaps in docs.
- closing out some issues and working on a few docs for networking, ebus, assets and stuff like that.


### Graphics/audio - presented by Tobias Alexander Franke
- Roadmap coming soon!
- There will be items that are mobile specific targeting optimizations for the Atom renderer running on mobile.
- The mobile group hasn't come together yet to discuss forking off the low end pipeline into a specific mobile pipeline.

### No representative or roadmap items posted for the following
* Content
* Operations
* Security
* UI/UX

## General questions

### Question from Royal OBrein (obwando discord)
Royal OBrein [LF]: As we have more people starting to come over from cross-pollination and awareness some are unsure why and where to get into SIGs. It may be helpful if the SIG readme could answer a few of these questions where they can be found...

```
How can people get involved in each area?
Where would they start?
Why is it important for them to become a part of your SIG?
Who would be interested in joining.
```

- why is it important for someone to become part of a SIG, what kind of person would be interested in joining?
- we have college students, vr people, game developers, and I think if we look at giving them an understanding of why the sigs exist and their focus areas... who can I talk to, ... finding a way to get them more involved in SIGs.  Recommend putting in the readmes in their repos.

byrcolin: What about videos?  (Discussion of a small youtube video)

Kadino: Sigs have charters and information in their readmes. We should highlight that there's no barrier to get started. 

Royal: I present 2 radios of 50 radios how quickly will you choose.

### GreerDV: I'd like to discuss the good first issue label.
- dg211  - if you go to issues theres a "good first issue" label, and it has a link, it takes you to a query that is based on the label "good first issue" label seperated by spaces, we have good-first-issue seperated by hyphens.  Its not clear its being surfaced to new users.
- sig build will look into renaming/or whatever is necessary to fix this.  No objection by TSC or other members present, its just broken and needs to be fixed.

### questions from byrcolin
- Remember to apply your processes to all canonical repos, not just o3de/o3de!  Is there no way to copy the initial setup of a repo?
- Mike Chang - the blast radius would be very large to do so automatically
- Royal OBrein  - we have scripts and tools to copy tags and issues between repos.
- byrcolin - the other issue is moving things from repo to repo.
- Nick_L Suggested a runbook or checklist for anyone copying a repo or making a new cannonical or deprecated repo to follow?
- Mike Chang  - Sig build can own the checklist/onboard/runbook.

### byrcolin  - Deprecated repos
- Mike Chang  Archive repo setting exists, we can use that and add it to the runbook / checklist
- byrcolin to generate the ticket for sig-build to work on this.


