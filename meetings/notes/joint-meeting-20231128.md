# Joint TSC : SIG Meeting 11/28/2023

# Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (by discord name)
* colinb[APMG]
* geds-dm [Amazon]
* Gl
* Joe Bryant [Amazon]
* JT [SCB_GameDesign]
* Luis Sempe [Amazon]
* Naomiwash
* Nick_L
* Nicole Huesman [LF]
* null
* RoddieKieley [Red Hat]
* Sergio Rojas
* Sid_Moudgil [Amazon]
* Steve P [Amazon]

## Overall outline
This is the "All sigs" check-in and roadmap review for the end of November.

### Agenda Topics
Github meeting issue: https://github.com/o3de/tsc/issues/104

#### SIG Updates

### Sig-Core Roadmap
SIG-Core Roadmap: https://github.com/orgs/o3de/projects/31
* Supporting tool applications in non-monolithic release
* O3DE engine Gem rename support 
   - It will have no audio though, WWISE is propreitary
   - JT - Another audio engine potential LabSound on GitHub
* Added a feature for users to tag allocators (see wiki  https://github.com/o3de/o3de/wiki/Allocator-Tagging-Guide )

### Sig-Release
- doing an internal playtest at AWS.  Use all the different functions (primarily prefab overrides)
- Would be awesome if other people here in this meeting can either convince their companies to spend some time or other people or advertise
- 29th is the point release testing date.
- This will be our second test - we did one last week and found issues, resolved issues.
- Linux, Windows, Arm can also be used (from source)
- SNAP.  For robotics it brings a lot of issues that even Canonical recognises as issues.  De-emphasising snap for linux.  
- Steve:  Re-thinking snap workflow in general, or dockers, or EMIs.  Marketplace EMIs.   Nick: Would docker be preferred for EMIs?
  Ideally the engine shouldn't be modified.  
- Steve:  Snap has its own confinements.  That project can only run in that snap container as well.  You'd have to install O3DE to run anything which you made on it, which is not ideal.
- Steve:  Docker - at least all those sample projects work.   
- 

#### Ad-Hoc topics to bring up?
### Steve P
* Ubuntu 22.04 is the support version but the docs list 20.04.
* We say arm64 is experimental - do we keep it experimental?  We don't have an AR blocking job for when it breaks.
- Discussion about arm64 being experimental:  Current consensus is to keep it experimental.  If someone breaks a build, we will not know.
- Naomiwash:  Suggest we write a 1 page proposal about reducing builds down and potentially swapping out platforms.  Could be a quick email vote.
- JOe:  We are slimming down and cutting AR mostly anyway, users will run it locally.
- Sig-build could do this.
- could add a node for arm64.
- the nightly (e.g. https://jenkins.build.o3de.org/blue/organizations/jenkins/O3DE_periodic-incremental-daily/detail/development/117/pipeline/1478) high bar is
  not critical to our needs.
- Joe:  It will become important, and would need to be green and report the correct status.
- People are still required to test locally. Output blurb that they are required to paste in.
- The costs do not currently scale as we get more contributors.
- ColinB - Consider having contributors contribute compilation resources.
- Joe:  Large open source projects should never have a member owning the CI/CD pipeline, what happens if that member decides not to contribute?  The foundation
  itself must own the CI/CD pipeline.  How do we make it efficient?
- Publish your PRs on github or just mention tests
- Post links to the downlodable builds in discord.

### Naomiwash
* Pressing for the OpenSSF Best Practices badge
* https://www.bestpractices.dev/en/projects/5536#quality 
* Can we deal with this, or find out what needs to be done to meet it?

### Action Items
- Nick stays to talk about miniaudio o3de.
- After the dec 5 point release, Joe will take a document that talks about where we're at with CI/CD, ownership plan, and solutions
