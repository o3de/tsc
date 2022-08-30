# Joint TSC : SIG Meeting 2022-08-30

## TSC Attendees

- Karl Berg
- Nick Lawson
- Royal O'Brien
- Jeremy Ong
- Tobias Alexander Franke

## SIG Chairs/Co-Chairs, Marketing Attendees

- Deepka Sharma
- Finchy
- geds-dm
- Joe Bryant
- lmbr-pip
- vincentvincent
- Yuyi Hsu

## [Agenda](https://github.com/o3de/tsc/issues/49)

### SIG Updates

Several sigs are gearing up for the next round of chair and co-chair elections for the coming period. If you are interested in participating either to nominate, run for, or elect SIG chairs or co-chairs, please check in with the leadership in the SIG of interest.

- SIG-Core
  - Continued improvements to the AZStd library facilities (ranges, data structures, math APIs)
  - (upcoming) Progress on the archiving system
  - (upcoming) Will proceed soon on investigating C++20 support
- SIG-Release
  - Preparation is underway for the upcoming October 2022 release, see [here](https://github.com/o3de/sig-release/discussions/52) for more information
  - Reminder to follow the established procedures documented in links in the above document for merges to the stabilization branch
  - (upcoming) Working on a proposal/process to track ongoing and upcoming changes/roadmap (see [here](https://github.com/o3de/sig-release/issues/79) for the proposal)
  - (upcoming) Discussion ongoing regarding alpha/beta release process (to be published as an RFC)
  - (upcoming) Continued refinements and documentation to the stabilization process
- SIG-Security
  - Python was upgraded to 3.10 to immediately mitigate various security issues and eliminate the need for maintaining certain package forks
- SIG-Build
  - The project was upgraded to support the MSVC v143 toolset, which is the default on VS 2022 and all CI builders on Windows were upgraded to the latest toochain
  - (upcoming) Documentation is being written to describe how to use the new toolset, and support for v142 is expected to be maintained for ~2 releases
- SIG-Platform
  - (upcoming) Working in conjunction with the Graphics SIG, progress in integratin OpenXR is still underway
- SIG-Networking
  - A number of improvements were made to the client-server connection lifecycle (disconnect/reconnect flow)
  - Improvements were checked in related to spawnables
  - Continued improvements to multiplayer test suite
  - (upcoming) Migration of AWS functionality to an external repo is ongoing
  - (upcoming) New multiplayer sample development and performance testing/optimization
- SIG-Graphics-Audio
  - The initial preview version of Material Canvas (node-graph editor for procedurally defined materials) is taking shape, with additional changes to material and shader handling on the way
  - A number of performance and memory improvements (ray tracing, texture pool)
  - (upcoming) Improvements to the culling and shader systems
  - (upcoming) Render upscaling solution based on AMD's FSR2 library
- SIG-UI/UX
  - Continued progress on RTE workflows including onboarding, character creation, multiplayer scripting, engine extensions, and more.
  - A holistic user experience survey of the engine was conducted
  - (upcoming) A blog post is being authored to communicate the results of the user study
  - (upcoming) Continued RTE workflow improvements and iteration

### General updates

- A number of conversations are ongoing with different devs to work on various vertical slices of content/code for the engine
- Several universities are adapting a more C++-centric game development curriculum and considering O3DE (e.g. [Kutztown University](https://www.kutztown.edu/))
- Ongoing discussion on mobile-positioning (WG vs SIG formation), given foundation participation of two large mobile IHVs
- Lots of work/prep towards the upcoming October O3DE conference

### Open Discussion

- A update was requested for the website redesign (Royal to followup with Nicole), which would include changes around how the new-user install/download flow would be presented
- A [question](https://github.com/o3de/tsc/issues/49#issuecomment-1231789061) was raised about guidance for addressing PR abandonment
  - Several suggestions raised regarding timing, but the conclusion was to keep timing window open-ended based on issue priority. PRs addressing critical issues with an unresponsive author could be addressed by a maintainer directly with a polite note. PRs addressing issues that the SIG intends on working on may be handled directly as they fall on the roadmap. PRs that have no acitivity with no intention for completion may be closed with a note suggesting the PR be reopened if the author wishes to engage again. Some guidance may be authored in the draft [CR guidelines doc](https://github.com/o3de/community/pull/144).
  - Another topic discussed was draft PRs in the same vein. A similar policy would likely apply, the only difference between a draft and final PR being that draft PRs are generally submitted with the intention of early feedback/conversation about the change. Without any conversation, the PR could be closed or taken over by a maintainer based on issue/feature criticality
