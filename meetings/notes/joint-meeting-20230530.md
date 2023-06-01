# Joint TSC : SIG Meeting 5/30/2023

# Chair and Co-Chair
* Nick_L[amazon] 
* Tobias Alexander Franke [Huawei]

these notes taken by geds-dm [Amazon] - thank you! (Chair Nick_L lost power during meeting)

## Attendees (by discord name)
* ColinB [apmg]
* geds-dm [Amazon] 
* naomiwash
* GI
* Royal OBrien [LF]
* HighFly (Fly Forge)
* Null [Amazon]
* Sid_Moudgil [Amazon]
* vincentvincent

## Topics

### Topic 1: Combined Roadmap:

See the below link for the topics for discussion this week and information from the SIGs

https://github.com/o3de/tsc/issues/80

Naomi: Can we restart and build on this?
    Changing/adding columns? (example: Goals, Possible Features of xx Release)
    https://github.com/o3de/o3de/projects/1


ColinB: Concerned about it an additional responsibilty that SIGs would need to add to their individual meeting process
gems-dm: Believes it should be simple to add an existing roadmap item to the combined roadmap project
Naomi: Brought up ways to try to reduce the burdan on each SIG
Sig_Moudgil: Wanted to know the granularity of what to share on the combined roadmap and has concerns about what a SIG can commit to for the next release
geds-dm: Mentioned only adding to the combined roamdap items that are completed or in-progress work that is almost complete and would certainly make the next release


The SIG-release group is having a release retrospective.
Should that release retrospective be open to all SIGs?
Should/Can one of the TSC office hours be used to have a one of and potentially discuss new features

vincentvincent: Brought up mentioning adding roadmap maintenance to the roadmap as part of the charater
ColinB: Doesn't think that should be part of the SIG Charter
ColinB and geds-dm CHow about adding a template that each SIG can start from that provides an instruction
guide on how to run the logistical operations of a SIG(How to run meetings, which broads to triage, which roadmaps to updates, etc...)

### Topic 2: Feature Grid Update:

vincentvincent: Does everyone agreee that the Feature Grid should be maintained? Also is there a way to streamline the process
Royal: Yes it gives the community a quick way to see the state of O3DE
ColinB: Provides a high level overview that is not too hard to maintain.

geds-dm: Are there ways to ease updating the Feature Grid matrix, such as automatically creating the PR for the user with the [Create Release Markdown](https://o3de.github.io/community/features/form.html) option
Royal: Yes, but that would require code.


### Topic 4: Attendance and Meeting Frequency

ColinB: broached the topic of attendance to this TSC meeting.
Should the time be moved or adjusted?
Should the frequency be changed?
Action Item: Naomi to reach out to SIGs about the meeting

## SIG updates

### Release - presented by vincentvincent
 - Roadmap at SIG Release roadmap: https://github.com/orgs/o3de/projects/29
 - Sig Release work done last month:
   - Released 23.05 in collaboration with other SIGs and gathered release feedback from the team.
 - Sig Release plans for next month:
   - Do the 23.05 release retrospective, and decide on the next item of improvement.
   - Together with TSC to decide whether we would want to mention the roadmap maintenance are one of the SIG responsibilities on the SIG charter. This is the issue that tracks this discussion: Add roadmap maintenance as SIG's responsibility on each SIG charter. sig-release#146
   - Start a discussion about the next release date.
  - Proposed Agenda item about updating the Feature Grid
    Challenges
        The features grid is one of the release deliverables. Updating the grid generally involves two steps. First, SIG has to manually update each of the sections that it owns, along with other release deliverables. Second, the SIG Community-and-docs converts the grid's JSON file into a document format (I believe it is a markdown). You can see what it looks like on the docs page here.
        Few challenges faced in the past two releases
            SIG needs to spend time manually maintaining the grid in addition to its other responsibilities. It also requires two approvals, which makes it even slower.
            The Release manager needs to persistently remind SIGs to update the grid as the task is often buried by other higher-priority tasks.
            It takes time for SIG docs-and-community to convert the JSON into the markdown format.
        Questions to be discussed
            It takes effort to maintain the feature grid. However, the SIG release does not have visibility of how helpful the feature grid is to the community. Given that condition, SIG release would like to open a discussion with TSC and other SIGs to make sure the feature grid is still important to be maintained and everyone agrees that it is part of the O3DE release deliverable.


### Core - presented by geds-dm
 - roadmap at https://github.com/orgs/o3de/projects/31
 - Work on the replacement Archive System is underway with the initial Archive Gem being merged last month
 - Updates to better support Remote Gem version continues as part of RFC Proposed RFC Feature Engine, Project and Gem Versions sig-core#44

### Networking (available on the agenda)
 - https://github.com/orgs/o3de/projects/22 is the roadmap

## No representative or agenda items posted for the following:

### Docs/Community
 - roadmap https://github.com/orgs/o3de/projects/15

### Operations
 - roadmap ???

### UI/UX
 - roadmap ???

### Marketing/Advocacy Committee
 - updates?

### Security
 - roadmap at https://github.com/orgs/o3de/projects/45

### Simulation 
- roadmap: https://github.com/orgs/o3de/projects/23

### Testing
 - roadmap link at https://github.com/orgs/o3de/projects/35/views/1?visibleFields=%5B%22Title%22%2C%22Assignees%22%5D

### Build 
- https://github.com/orgs/o3de/projects/39/views/1 

### Graphics/audio - presented by Sid_Moudgil
- Roadmap https://github.com/orgs/o3de/projects/41
- Work on Shadow Cascade Optimizations is being done
- Added VMA buffer and D3D12MA support

### Platform - presented by ColinB
 - https://github.com/orgs/o3de/projects/20
 - Not any roadmap item updates for SIG-Platform

### SIG-Content
 - roadmap ?
 