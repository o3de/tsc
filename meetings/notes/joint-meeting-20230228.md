# Joint TSC : SIG Meeting 2/28/2023

# Chair and Co-Chair
* nick_l[amazon] 
* Tobias Alexander Franke [Huawei]

## Attendees (by discord name)
- geds-dm (Amazon)
- kberg [Amazon]
- Mike Chang [Amazon]
- Nick_L [Amazon]
- Tobias Alexander Franke [Huawei]
- tomhh (hultonha) [Amazon]
- JT [SCB_GameDesign]
- RoddieKieley [RedHat]
- Seapip [Amazon]
- Kadino [Amazon]
- Chanelle [Amazon]
- Alex P [Amazon]
- Vincentvincent 
- ThatHighFly

## General Updates and Announcements
This week's ticket: 
https://github.com/o3de/tsc/issues/70
"All sigs project boards link" - https://github.com/orgs/o3de/projects?query=is%3Aopen+SIG

## SIG updates

### Networking - presented by 
- https://github.com/orgs/o3de/projects/22 is the roadmap
- Large contribution of a third person multiplayer sample game driving a huge amount of changes in the base engine
- Lots of performance fixes, client side connectivity, ease of use, other things to do with seedlists, everything else.
- hoping for march submission for next release.
- open sourced as multiplayer scaler project for testing and perf testing.  Scale up to 500 clients in a hosted service in the cloud.
- planning to make it easy to redistribute server builds - coming feature.  next couple of months
- held new options (Karl and Pip re-elected as Chair and Co-Chair)

### Simulation - presented by tomhh
- roadmap: https://github.com/orgs/o3de/projects/23
- I added some updates from our side, big PR from huawei that have been dealing with manipulation in robotics.
- They have been taking a particular approach using joints.  Simulation robotics focus - RFC introducing articulations to O3DE
  and ROS2.
- Another RFC allowing transforms to not inherited in the heirarchy, which will allow authoring of robot arms simpler.
- Compliant contacts (grip strength, other related features). Added roadmap initiatives for those things.  
- Further out: Softbody physics - picking up things that have compression to them, deformation of terrain.  Maybe later this year?

### Security - presented by Pip
 - roadmap at https://github.com/orgs/o3de/projects/45
 - No update.

### Core - presented by geds-dm
 - roadmap at https://github.com/orgs/o3de/projects/31
 - Require additional nomination for sig-core chair.
 - Looking to investigate developer iteration speed - reduce build time, reduce number of items you need to build (split libraries),
   convert to dlls, reduce core gems in o3de repo, performance improvements to expensive systems like serialize/behaviorcontext.
 - Looking for interested individuals in sig-core

#### Questions:
 - TomHH tested removing slices, it was a sizeable difference, several minutes to build time.  Its a complicated process to untangle it
   and a promising investigation.
 - geds-dm to follow up.
 - TomHH: Also the old cry math library.  Quite a bit of code, very delicate thing to remove, but it could be a long term plan to get rid
   of that, 3 to 2 math libraries.
 - LyShine is the primary stopping point for removing slices.

### Docs/Community - presented by Chanelle
 - roadmap https://github.com/orgs/o3de/projects/15
 - Meeting cadence 1x month first tuesdays
 - Resolving an issue to make roadmaps discoverable from the documentation. (Different from discoverable from website)
 - ROS2 docs, other docs coming in for review.
 - Another process we're trying to resolve is how to improve our gitflow (commits going into main and devl).  Treat each commit into main as a hotfix and then everything goes into dev.

#### Questions for docs/community
 - Mike Chang: Main is prod branch - everything pushed becomes public? (Yes).  For the website and releases there is code that will push between development and main.  
 - Seapip:  docs have a different challenge - 2 live forks, main is against latest weeks and needs to be patched.  Dev where people pull updates.  The short term is either you have someone who weekly sweeps main changes back to dev, or you're asking main contributors outside release flow back to dev.  
 - Mike chang:  it may require humans due to context needed.
 - Chanelle: don't need full automation, perhaps only partially.  Was curious about how it would be done without huge PRs.
 - Nick: Should we put new docs in dev, then wait for them to go to main?
 - Chanelle: Put it in main and dev (?) since it can be 6 months between release.
 - Pip: Sounds similar to stabilization and then cherrypick to dev.  Maybe a weekly merge?
 
### Release - presented by vincentvencent
 - Roadmap at https://github.com/orgs/o3de/projects/29/views/1
 - Last month:  
    -  All except security and ops now have a roadmap!
    - Discussing which repos are included in the releasae process (o3de-extras).  Discussion is ongoing
    - Sig-docs discussion to surface the roadmap in the main website and documentation website.
    - Next release 23.05 - may 3rd 2023
    - start stabilizing by march 15th at 10am PST
 - Next Month:
    - Start the 23.05 stabilization process.  https://github.com/o3de/sig-release/issues/133 for comment
    - work with docs/community to surface roadmaps.
    - Decide the criteria for repositories to be included in the release.  O3DE Extras.
    - Complete the documentation of the Release Process itself.

### Testing - presented by Kadino
 - roadmap link at https://github.com/orgs/o3de/projects/35/views/1?visibleFields=%5B%22Title%22%2C%22Assignees%22%5D
 - In game test automation proposal - RFC 
 - Getting public metrics - a proposal will need to go to the group and TAC for extra infrastructure spend.
 - https://github.com/o3de/sig-testing/pull/66

### Build - presented by Mike Chang
- https://github.com/orgs/o3de/projects/39/views/1 
- Sig build is working on profiling the entire build.
- RFC to propose to reduce the cost of AR by migrating the items into github actions. the benefits around that, open to any feedback on that.
- https://github.com/o3de/sig-build/pull/79
- huawei was trying to merge in a commit that was targetting an aspect of windows that is not available in the current release of a min-spec  win 10 but is available on win11.  Its now a roadmap item.  Bump up version to at least 20H2 (windows 10 updates).  Target version was windows 11, we have a policy of windows versions to support.  But probing everyones opinion for minspec win 11.
- Looking for contributors from the "outside" to manage the roadmap.  The question about that is how we can add organizations and partner orgs
  to the roadmap management and other management such as add to a branch with multiple contributors.  For example wanting to make a major branch
  in the main repo.  Its happened a few times already, the O3DE repo should only have the development, main, and stabilization.
- JT - Several projects in AWSF discuss them.

### Graphics/audio - presented by Tobias Alexander Franke
- Roadmap https://github.com/orgs/o3de/projects/41
- Material Canvas
- Multi-view rendering
- Buffer allocation AMD library
- Mesh instancing
- In progress: Prototype multi-gpu support (Branch that we've just been talking about - Huawei)

#### Graphics / Audio questions
 - Tobias - Is there a plan to move to Qt6?
 - Feature for raytracing commands only available at certain versions of directx for windows update.

### Platform - presented by RoddieKieley
 - https://github.com/orgs/o3de/projects/20
 - Wanting to get another linux distribtion up to par with ubuntu.  Redhat efforts to get some resources in Fedora.  

#### Questions for platform?
 - Mike Chang: Yum package?  A: Fedora upstream main, eventually redhat.  To become a part of the distro, yum install you need a bunch of criteria.  All buildable from source and all licensing restrictions must be solved.  So unoffical RPM and then full licencing compliance.

### SIG-Content - Alex P:
- Announcement, canonical o3de.org repository inside the o3de github group of repos.  Intention is for official approved remote repos, remote gems, etc.  The currently has OpenXR, and one other.  What we'd like to do is make this repository available by default in the project manager but right now we can't do it but hasn't finalized this approval process.   But we have an upcoming release.  Talking to Royal about it, we all seemed to think is a good one.  We enable this repository by default, but its empty.    We can over the next 6 months get the approvals and get it in the project manager.

### No representative or roadmap items posted for the following

* Operations
* UI/UX
- JT [SCB_GameDesign] - I really encourage to everyone to interface with them.  Really streamlining and optimizing their process to help you work with them as efficiently as possible and touch base with that team.
- NickL See https://docs.google.com/document/d/1A8nm1tHmbPLN4F6Wu0WtHv-YxgrLwIoxxwNkhT6b3O4/edit

## General questions
(Question about reputation)
    - ThatHighFly - suggestion to the marketing team to improve the reputation and view to draw people back, (paraphrased here, due to time constraints - concerns are around winning back the reputation lost by initial rollout)
    - JT [SCB_GameDesign] - End users were jumping in without reading the website and document and intentions were mismatched.  We are having to repair mistakes.  Very experienced in how blender development, I've run the most popular soft-fork for blender.  The misperception (plus I have a background in marketing) is that its for users to jump in and use when it is in fact an invitation to developers to help build it.
    - NickL: General call to Get Involved, especially with UI/UX
