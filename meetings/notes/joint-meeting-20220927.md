# Joint TSC : SIG Meeting 2022-09-27

## TSC Attendees

- Karl Berg
- Tobias Franke
- Roddie Kieley
- Jeremy Ong
- Royal O'Brien

## SIG Chair/Co-Chair Attendees

- geds-dm
- byrcolin
- bhanuja-s
- Joshua Rainbolt
- Tony B

## General Updates and Announcements

- SIG chairs and co-chairs are encouraged to use the Github Roadmap tool to manage your triage process and facilitate issue/pr visibility
- An o3de-extras repo is available to host O3DE-maintained code that not all users may need. While the content and functionality in o3de-extras is optional, SIGs are expected to include issues and PRs filed here in their triage and review processes
- Please submit feedback/comments to the active mobile-platform focused SIG discussion here: https://github.com/o3de/tsc/discussions/46
- ROS integration in a gem is being brought under the foundation as an actively maintained community project

## SIG updates

### Graphics/audio

- Added support for image mip streaming (partially resident mipchains and eviction)
- Stereoscopic rendering support for VR
- Continued progress on material canvas and pipeline abstraction

### Release

- 2022-10 release is making progress and work is underway to finalize release notes and documentation
- Stabilization effort is ongoing with 15 active/open issues: https://github.com/o3de/o3de/issues?q=is%3Aopen+is%3Aissue+milestone%3ARelease%2F2210
- Issues must be closed out by 2022-10-05 to be tested in time for the release on the 11th
- PR and marketing set to publish release materials on the 13th
- Runbook for a release is planned for a release later in October
- Changes/updates to the feature grid are in progress (communication TBD from Vincent)

### Networking

- A number of UI changes and improvements have been merged to improve usability of network components
- Networking related metrics are exposed now to facilitate debugging and troubleshooting workflows
- Work is continuing on splitting code to ensure that server-only code doesn't ship to the client
- A new multiplayer sample is in development, with the aim of being a useful project template to get up and running with content and best practices sooner

### UI/UX

- Bhanuja was elected co-chair and is starting her responsibilities
- UI/UX roadmap is visible here: https://github.com/orgs/o3de/projects/9
- A usability study was conducted with the results posted here: https://github.com/o3de/sig-ui-ux/blob/main/user-research/2022%20Q2%20O3DE%20User%20Experience%20Survey.md

### Core

- Elections for the SIG Core chair and co-chair will begin next month
- Core libraries are being split to improve binaries sizes
- C++20 usage investigation is slated for next year, contingent on restricted platform support
- RFC for semantic versioning of the engine framework and gems is in review