# TSC Meeting - 4/30/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* drakeredwind01 [cyber-sec, idea]
* Gaian Helmers [Genome Studios]
* jjsteele [Bay Software]
* Joe Bryant [O3DF]
* lemonade-dm
* Luis Sempe
* naomiwash_lf
* Nick_L
* null [meta]
* RoddieKieley [Red Hat]
* Steve P [Amazon]

## Agenda items, All-sigs-portion
https://github.com/o3de/tsc/issues/121

### Sig-Core: Lemonade-dm
* update for the next month - new work that will be coming in.

### sig-graphics (Sid)
* Big update for mobile side - all the rendering pipeline work and performance work for the carbonated game is now merged
* automated testing on a mobile device should be quite performance.  
* Device rules exist, you can set tiers/platforms
* New features for the mobile pipeline, but you could use them for the main pipeline too - gobo lights, shadows from 'simple' lights
* Culling from lights, lots of shader management console updates.
* Eventually it would be nice to do a video on doing mobile releases and how to make a mobile package and set up the performance tiers.
* There's also work on smaller sections:  Meta checked PR for merging tiles and skybox pass for the VR pipeline, 20% improvement in perf.  We can leverage that for the mobile pipeline once merged.  Lots of works going in for fixes from Huawei on the mobile side, they are working on the MGPU.  They will hit after the release branch is cut.  They will change every single object in atom.  This will add it to the RPI, it will be active under the hood by every pipeline.  Hit dev in the next few weeks.
* Talked with Robotec-AI folks on how to do shader performance, how to build shader permutation lists, etc.  More should probably be published.  Keep an eye out.
* Joe:  In general, I am seeing generally, apparently this team called VirtuOS integrated a flexible virtualized geometry for O3DE.  They implemented it and created a gem for it.
* Meshlet gem is a core pillar, it uses direct draw calls, its not fully indirect.  For truly virtual geometry you need a lot more than just whats in the meshlet gem.  Each stage is a huge amount of effort.  Apparently, Huawei continued on the path starting from the meshlet gem, almost at level or better than Nanite.
* Joe: I'll talk to them about it.  I meet with their head of open source.

### sig-platform - Steve P
* removed references from Ubuntu 20.x
* No changes required for 24.04
* Initial test builds seem to be fine, no special changes required.
* Libc controls the backward compat.  So we still build on 20.04
* 24.04 Clang is version 18.  Looks like its fine?

### Sig-release update from Joe
* Postponed the release to next week - there were 2 last minute issues 
   * one being a crash whenever you do a full clean with the AP
   * the other being the demos run with the wrong settings.
* SteveP: AP crash verified on windows.  Related to asset browser.  We should fix it.
*   Nick: I'll fix it.
* 10am next tuesday, sig release meeting.  Release will be done.
* Readme.md updated, roadmap links now included
* Naomi and I looking at how we want to change the O3DE site to point out the roadmap etc.
* Joe: Friday: Roddie is going to give a session on how to update documentation.  Gaian and Shauna are going to create an intensive video on how to update documentation as well.   Promoting the docs up to mainline for release.  

#### Questions

* Nick Q: docs?
* Sid:  We need to add a page about all the pipelines - main, mobile, vr, etc.  You can swithc between them in the editor you can set them using a cvar by default, this will be set by default.  You can control which one is set, you can control it with the tier system. T here is a whole organic talk about releasing this thing, but we need some docs.  Throw it on the wiki page, and you can switch between pipelines, capacity and so on.

## Agenda Items, other

### Joe: Maintainer Structure Discussion
* Large open source projects want a hierarchy of maintainers.  We need a lead maintainer.
* Lead maintainers are tie-breakers, or can coordinate implementations, etc.
* Other people like nick, lemondae, colin, sid, luis, etc, who can actually make calls about things and get things done.
* We should have the one maintainer who is the lead maintainer.  Peoples thoughts?
  * Roddie:  Makes a lot of sense - the technical operation of hte project is different from the outside coordination.
* colinb[APMG] - have there been any situations?
* Joe Bryant:  Yes, there are a couple situations, and there will be some contentious items to propose in the next few months.  Plus its good to have such a person identified anyways.  We are growing, new users are starting to grow, we're getting a lot more PRs, growing like crazy.  We're starting to see O3DE everywhere now.   We do a weekly O3DE search showing up in all sorts of spots and more often.
* There are a lot of other projects that I'm basing this of, they have at least 1 lead maintainer who can make final calls on things.
* Having someone that has a final say.
* null [meta]: Why not bring it to the TSC meeting?
* TSC authority and ability to make decisions will not be undermined
* Some times we need an immediate response, its good to have a person that knows and can make a quick decision.
* Joe Bryant: seeding the idea now, in probably a month or two, I'll bring it up again [O3DF]
* lemonade-dm: I wouldn't want it to be in the hands of one person.   Active/knowing about the project/contribute/maintainers.
* Joe:  Maintainers would have to figure out who that person is, someone I trust and the TSC trusts or to provide input.
* Joe:  I have to make a decision I don't have all the tech knowledge and O3DE is gigantic, need people to ask with a fairly quick response.
        The maintainers are very close, have the pulse of all the code happening, whats good and whats not, etc.
        Particularly with the security issues coming in, trust is an important aspect of that.
* null: When we founded the TSC we got a charter, https://github.com/o3de/tsc
        Maybe we should @ping people and get quick responses?
* Joe:  You're my emergency go-to for core, Sid is atom, and I have nobody for emotionfx.
        I'll ping maintainers, for now.
* Joe:  I want to prune the maintainer list down as much as possible.  we need to think on this
* Joe:  I'm going to put together an actual written document that people will take a look at, one of the TSC meetings, 
        probably early june.  I'll present to the TSC and show what I'm looking for, we want a small group, or one leader, we need an easy
        way to contact maintainers and need their input.  We can narrow it down on each part of O3DE.
        Based on colinb, nick, lemonade-dm, null, I think that I will start by having an easy way to contact maintainers when an emergency happens.
* Gaian:  Can be fixed by workflow adjustments...

### Joe: Future Planning, Discuss how the community wants to determine future of O3DE
* Joe:  O3DE is gigantic.
* Potentially taking the renderer and making its own project under the O3DF.  It would still be part of O3DE, but maintained as a seperate project.  Expertise for the renderer is completely different from the rest of O3DE.  Different maintainers, different ways to develop, etc.
* I have a lot of companies that are interested in the renderer and less so in the engine its attached to.  Foundation benefits and O3DE benefits are still good because it gives us a lot more potential contributions back that also gets the foundation more members, which is good overall, since then the foundation can do more contracting and so on.  We need to go where the footsteps are instead of carving our own niche.  We get questions about the renderer all the time, for example godot could pull it in.  Ultimately that benefits us (O3DE), if people can take the renderer.
* Joe:  The whole point of this is just to start investigating.  
* Null:  Look at this from the inverse perspecitve.  Remove everything from it thats not required for the render.  We have internal pipeline and build tools here at meta.  How would we fully integrate o3de into some of our research pipelines.  What are we going to do about cmake?  Huge lift to decouple it.
* Joe:  We should start with research, how big of a problem is it, is it even possible, etc.
* Sid:  It was developed in isolation, and then plugged into O3DE.   You're going to need a strong use-case.  A couple companies are going to want to take the part they need (a good PBR renderer).  O3DE SDK thats just the renderer, potentially.
* Sid:  Its split into many gems.
* lemonade-dm:  O3DE exists as a SDK.  You can take the O3DE SDK as a whole and split it apart, you can for example make an installer that only has atom.

### Joe:  On the AI, policy on the contributions from AI.* colinb:  Suppose you want to support just a console application, you'd

* We don't have an actual policy but we have guidelines.  Most open source companies are trying to be good citizens about how we implement AI.  One of these is how hte LLM is trained.  It needs to be trained on open data, not copyright data, etc.  Rules around that.  Right now, for the AI, we are plugging into different system, we are not creating our own LLMs, as we have usecases that might change.
* Joe:  Should we allow someone who has said to use an AI tool like this to contribute to code.
* Joe:  Examples of bad actors are consistently using copyright or protected code in o3de, wrong licenses, someone whos putting security vulnerabilities in their code, backdoors in their.

## Action items
* Joe can put up items for people to work on that we need.
* Drakeredwind01: How can we make it interesting?

