# Joint TSC : SIG Meeting 6/27/2023

# Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (by discord name)
* Nick_L
* colinb[APMG]
* drakeredwind01 [cyber-sec,idea]
* geds-dm [Amazon]
* Kadino [Amazon]
* Naomiwash
* null [Amazon]
* RoddieKieley [Red Hat]
* JT [SCB_GameDesign]
* Sid_Moudgil [Amazon]
* Tony B [Amazon]

## Overall outline:
The overall outline of this meeting is posted here, but a recording is available for details
* Recording ID: gYX6YNvLRo

### Ad-hoc topic:  general guidance for sigs
* Naomiwash discussed the "O3DE SIG + Documentation Processes" doc https://docs.google.com/document/d/1b-g1tAjDwMmEBzGBZ34OBTlBk-InUWxNzUqLJI-uNkg/edit
* Please review or comment on the doc!

## All-sigs reporting in:
See the below link for the topics for discussion this week and information from the SIGs
https://github.com/o3de/tsc/issues/84
 
### Sig-Release - Presented by Tony B
SIG Release updates can be read here
https://github.com/o3de/sig-release/issues/200
#### What we did last month

* Held a 23.05 retros session with the TSC and SIG Chairs You can see the retros result here.
* Brought up a discussion about the features grid and whether it's going to be maintained going forward. Nick from the TSC will own the next step as stated in the retros feedback.

#### What we're going next month based on the roadmap: https://github.com/orgs/o3de/projects/29

* Follow up retros action.
* Complete the SIG chair and co-chair election process 2023 - 2024.
* Start a discussion about the next release date, release manager, and how to keep the release quality bar without dedicated QA.

Sig-release is finding a release manager and will be having an election in July.

### Sig-Core - Presented by geds-dm
Here is the Roadmap for SIG-Core: https://github.com/orgs/o3de/projects/31/views/1

Updates since May 2023 Meeting:

* The new Archive System work has been submitted to Development
* Support for writing the new archive format has been added as PR: 
see https://github.com/o3de/tsc/issues/84 for links to individual issues.

* Additional support for being able to use the import directive in settings file
* new projects will be able to use CMake presets
* new settings registry support for specific launcher types (seperate settings for server vs cloud)
* stabilizing release builds - specifically monolithic releases for windows and linux.

### Sig-testing, presented by Kadino 
* Not a lot of contributor activity

### Sig-network, presented by null [Amazon]
* Running load tests, performance-wise, having an engineer putting that test together and get the numbers out.  The major lift has been gamelift 5 integration, and preparing for some public testing of the sample game.
* Gamelift integration is complete but not sure if committed to the public repo yet.

### Sig-graphics
* Shader converter that apple released to simplify metal.
* Custom resolutions and DPI scaling support, ability to change the render pipeline in the editor itself.  Functionality is added but trying to address all the edge cases.
* Externally working with huawei that added multi-gpu support, ongoing effort but its going to PRs right now and at some point in the future we will have RHI support on multiple devices.  
* Other work around bugs and issues.

### Sig-platform
* Engineer on Red HAt is focused on fedora O3DE and going thru and breaking down all the licensing requirements between what fedora woudl be able to accept vs what is present.  Try to get a RPM package to accept into long term upstream fedora.  Its going to be a multi-step process.  

## General topics

Naomiwash: Asked for further clarification about what is in the release?
Tony B: Concern about the frequency of release, but I would love to have a release manager.  One reason why we're trying to make the elections soon in July, so we can secure a release manager and no transition of sig chairs during the release.
drakeredwind01:  I was talking to networking & security about making a release.  There are some legal issues around the release.
Tony B: Not aware of the concern.
drakeredwind01:  Gene from Amazon might have more information.
Royal OBrein:  Legality?
drakeredwind01:  Something about providing an EXE for a release something might happen in terms of responsibility.
Royal OBrein:  You don't release the binaries under the same as the source code to help disentangling.
(Discussion about legal issues and how the O3DE Binaries is a separate LLC).

drakeredwind01:  Issue to allow me to add tags in the triages.  I have to make the suggestion and someone like Gene can do that.

Sid_Moudgil: how do non-amazon folks upload 3p packages.?  Release team may be required.
(Discussion of 3p package systems, please listen to the recording!)

## Action items
* Review the "O3DE SIG + Documentation Processes" doc linked above.
* Understand who owns the keys to update 3p packages, and do something with them.
* https://github.com/o3de/sig-build/blob/54982f610107b101d5e17b3aba30d711c7e729dc/rfcs/rfc-bld-20230302-1-3p-development.md

