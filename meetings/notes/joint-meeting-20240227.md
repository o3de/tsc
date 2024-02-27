# Joint TSC : SIG Meeting 02/27/2023

# Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (by discord name)
* Adam Dabrowski
* colinb [APMG]
* geds-dm
* Joe Brant [Amazon]
* JT [SCB_GameDesign]
* naomiwash_lf
* Nick_L
* null
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amazon]
* Steve P [Amazon]

### Recorded Meeting
* This meeting is recorded, for exact wording see recording.
* recording at: https://drive.google.com/file/d/1gR9id6-y86HYwcjzZGCBBSgWROPoo90L/view?usp=drive_link
* The rest of these notes is a brief summary.

### Overall outline
This is the "All sigs" check-in and roadmap review for the end of November.

### Agenda Topics
Github meeting issue: https://github.com/o3de/tsc/issues/113

#### SIG Updates

### Sig-Core (geds-dm)
* Movement of Gems outside the repo
    * Audio/WWISE is being removed from o3de repo and moved into extras
    * colinb [APMG] : What was the reason?
    * Joe Bryant: Moving core gems outside O3DE.  Temporary - we need a long term place for commercial gems, like for example putting AWS gems in AWS
      repo.
* colinb We might be referring to the gems not by name, maybe in the multiplayer project.  The instructions are convoluted in terms of copying a gem in place.
* null: This was a significant problem for onboarding, lots of complication.
* (Discussion about repos, repo system)
* colinb:  The repo system needs a lot of work.
* colinb:  Conflation of the o3de object system / what gems are required to be used.
* colinb:  Unfortunate decision that was my fault that was to mix the concept with external directories and gems. (I'm working on this, with schema 2.0)
* Joe Bryant: There is an auto script from Alex that lets you basically release gems and repos automatically.
* Reach out to Alex asap to find out info

### Sig-Simulation - Adam Dabrowski
* Robotics ROS2 gem, there is constant pace of work, mostly with fixes.  Steve has an important update with Physx5 Gem.
* Breaking changes with ROS2 Frame component
* Fixing and restoring python tests, unit tests, etc.
* Important cross interest group feature of GENAI framework gem.  Initial RFC is over, but this will be shortly followed this week with more technical details.  Due to formal reasons its not public yet, but its a Generative AI Framework Gen.  it uses reflection, behavior context heavily.  We are working on a POC with Layouting - automated creation of a scene from assets as specified by natural language.
* Next TSC we will be able to show more updates.
* Note about split of Physx5 / Physx4 - unlocked the installer to build simulation projects.  Now you can build Sim projects with it.
* One proposition that will come with the RFC would be to document the reflection better. Use the tooltip / metadata parameters for more documentation about it.  A topic maybe for keeping that inline with doxygen.
* Colinb:  what model is the AI using? 
* Adam: probably a mistral, llama model gem, etc.

### Sig-Graphics Audio - Sid Moudgil
* Mobile pipeline
    * A lot of work has been done for the mobile pipeline.  Its not in DEV yet, but will be.  
    * We have to figure out the timeline to bring from the games repo into the main repo.  We wrapped up the last few features - global lights (projector light), support for deferred fog, CPU culling on decals, lights, and so on.  
    * Trying to make it more performant.  Last few tasks are to make it use more of the shader variant system - so we added about a hundred variants to the standard pbr, and about 50 variants to the base pbr.   We fixed slow loading and memory issues due to materials.
    * Now we're looking at other performance improvements on top of that.
* OpenXR
    * RFC for XR Space, XR input, all the stuff around that.
    * Presenting at O3DE Connect, in march.  Meetings are in the morning at 8am PST.
* Multi-GPU
    * Work going on by Huawei.  Work is mainly in their branch.  RHI has been mostly ported over to support Multi-GPU
    * RPI you can't really do it in phases, they have been doing a lot of work to switch the whole RPI to use Multi-GPU objects.
    * One day they will put up a PR for the whole flip for RPI.  That will be a very hard PR to review (A lot of testing).
* Joe Bryant:  O3DF has contracted someone to help get those PRs up?
    * Sid: There is a contract, this person mainly working in the mobile space.  The Shader variant system is too complicated, now we're sort of pivoting a little bit (At least, I think we need to pivot).  So for example if you're on mobile, etc, then we can use a feature to reduce the complexity and allow you to build variants at runtime.   
    * Also looking at better foveated rendering, perf work, etc.
    * Also looking at mobile performance work, or at least investigating.
* Joe:  Before GDC we will make the roadmap public.  We want to talk about it at GDC.
* colinb [APMG] - a vulkan only renderer?
    * Sid: No, its a possible replacement for the shader variant system - if you are only running on vulkan, you can do shader constants feature, and build the variants online instead of pre-build.  It can explode to millions, trillions.
* Joe:  Now we need a particle engine
* JT [SCB_GameDesign] - looked at all the particle engines and most seem to be 2d instead of 3d.
* Joe:  What I was thinking was to investigate lumberyard's particle engine as an initial pass.
* colinb: Particle systems - what the lumberyard one was based on.

### Sig-Platform - colinb[APMG]
* Meetings are back directly after this meeting (so 9am PST Tuesdays)
* Platform deprecation for Ubuntu 20.04.  
* Steve was successful at building on 24.04 with minimal changes.   Naming differences, etc.
* Joe:  Starting to get questions on console, forwarding to (colinb)

### Sig-Release - Joe Bryant
* We've started the process but don't have the date yet, for next release. (2023.10.3 release tenatively)
* Performance and stability improvements, specifically around te DPE.
* Investigating and resolving issues
* Mobile is delayed enough that I won't be comfortable enough with releasing with timeframe around GDC.
* Still determining what goes in that release.  I will send out communication.

#### Ad-hoc
* colinb : overlo3de.com is semi-functional.  You can try it out.
* GDC
    * Naomiwash_lf: I don't have much updates since last time.  booth planning is done.
        * Live demo schedule is done
        * If you all are in the area and want to stop by and want some booth hours let me know.
