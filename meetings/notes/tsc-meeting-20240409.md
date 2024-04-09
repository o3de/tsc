# TSC Meeting - 4/9/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* adam Dabrowski
* colinb[APMG]
* Gaian Helmers [Genome Studios]
* Jan Hanca [Robotec-AI]
* Joe Bryant [O3DF]
* lemonade-dm
* Luis Sempe
* Michal Pelka
naomiwash_lf
* Nick_L
* null
* RoddieKieley [Red Hat]
* Sid_MOudgil [AMzn]
* Steve P [Amazon]

## Agenda items (Ad hoc) 

### Agenda Item: Joe Byrant - Release planing and cadence
* Mike C will be helping with the infrastructure
* April 30th tenative release 23.10.3 - bugfixes, optimizations, no features.  Cherrypicking FEATURES is too impossible.
* May 1st - Stabilization branch for next major release, slated for September due to the amount of testing required.
* Targetting September, but we will only release when stable and should go out.  We need to make sure anything we state goes into main does not regress in stability.
* Colinb:  Have we got together a testing process we can distribute?
* Joe: Partly, one of the things I'll do is a CTA, for the point release its primarily using the asset browser and editor.  Thats where a lot o our bugfixes are concentrated.  For the next major release, I have to put things together.
* Is the April 30th release still open for bugfixes or should it freeze?
* Joe: I should freeze it - contact myself or Roddie and we can make a determination.  For the next release we will make a stabilization branch for o3de-extras.  But it should only contain bugfixes that are compatible with the point release branch.  A little difficult for Robotec.AI because we have to be careful what we cherry pick from O3DE-Extras point release.
* Jan: We didnt' plan anyhing big for extras - just some fixes for the assets and duplicated assets between project templates / asset gems.
* Colinb - all canonical repos are part of a release
* Joe:  we have to be really caeful with the point release - we can't afford to have something that depends on DEV going into a point release.
* colinb: All of our releases should have a staging in every canonical repo.
* Gaian:  The Extras repo - my collegue Shauna has pushed an update to the multiplayer template can run and connect.  Not sure if the lines up but its there.

### Joe question for colinb
* Joe getting a lot of questions about free assets.
* colinb got the DCC tools - kind of expensive.  Some of the assets are not in great shape, sometimes they will be just the blender file, sometimes just be the output file (FBX model file), have to recreate them.
* Joe:  Prefer to be done in stages - whatever state they're in, lets get them up so that people can do it.  That way you can pull the entire community in to do it, and get it to a better state rather than just relying on yourself.
* Joe:  Not doing it myself, just taking a couple, making sure they work, etc, getting the structure down.  not trying to do the entire terrabyte at once.
* Joe:  Getting the first one up ETA?
* colinb:  Barring anything that is wrong on the store, I would say by the end of the month... 
* Joe:  we have other contributors interested in hosting the assets.
* Joe:  Lets focus on the ones that are already ingood shape and get those up asap
* colinb: I have enabled gitlfs, get it all stood up, get the package system in the right structure.
* Joe: Gaian and Naomi have asked about the assets and have a lot of experiences for processes about this.  My gut tells me lets get the stuff up and get the community to swarm on it.  Should say "these are lumberyard assets lets swarm on getting them converted to O3DE".  The fact that we have high quality assets, even if people have to convert them, its a huge deal.  What do you think ,Gaian, Naomi?
* Naomi:  does the repos already exist or does this have to be something we work on?  
* Colinb: no, not yet
* colinb: Does someone want to host their own store?
* joe bryant: No, better that then people sifting thru 1 tb of data on a repo...
* Gaian:  colinb: we are also appraching doing a market of our own, the idea was that would stimulate the community by providing this.  I would imagine we're doing an individual uploads.  We're still going to be a while, still have to do all our infra and stuff.  Community swarms on it.  Source-->Destination which colinb and I can draw from.  We can do some supporting stuff and helping.
* colinb:  We should centralized them as unfinished assets on overload, mirror those assets to your store.
* https://overlo3de.com already exists.

### Jan Hanca - Robotec.AI - AI sim and genai
* I need some ideas to proceed - sig-simulation, we published an RFC for Generative AI Framework Gem.
* We are ready for the code to publish, but where to put it?  extras?  main o3de repo?
* we want to publish and share with the community, it makes them less visible to keep on private repos.
* JOe:  Been talking with people in LF, or external, or making our genAI efforts a different project under the O3DF rather than O3DE.
    * O3DE would be first customer, but again, long term plans, learning how it works, how ot create a seperate project under O3DF, but genai might baloon to omuch to be part of the O3DE.
* null:  There is a lot of value in what he's proposing, without saying too much we have packages for other engines that allow integrations into llamas, chatgpt, anthropic, but also image synthesis, TTS, STT, drop one into your engine, drag a component onto entity and you have full integration.  Heavy as fully seperate foundation...
* Joe:  managed separately from O3DE.   But I still need to figure it out.  O3DE is gigantic to manage moving forward, its big, heavy, larger codebases for the open source foundations.  If we start adding a whole separate thing for GenAI which will grow in scope a lot, it will be too much.  I also think it limits the scope, if we put it in o3de extras ,it will be an o3de-only interface, for GenAI.  Which might be fine initially but lets figure out long term.
* null:  Our tools are managed by 1 guy part time.  Its the level your investment is looking for, its like, a tool that interfaces with those models and marshals data back an forth.
* Joe:  For now, host on o3de-extras for next release, however, for stabilization, we can get in what you have, no feature work after may 1 early june.  AR/VR stuff is getting in early june.  But the O3DE-extras is getting overloaded a lot, I want to talk about what makes sense longer term, 2025+.  But I think o3de-extras is getting overloaded with stuff.
* Joe:  don't wait until its "ready".    RElease early, release often.
* Gaian Helmers [Genome Studios] - Disconect between community led repos. Volumetrics Clouds gem.   Community index.
* Joe:  We have talked about community index...
* colinb[APMG] one of the reasons I made overlo3de, if I made a core kind of things, put it in a core or canonical repo.  However, that does incur the process (release, maintiners, etc).  They are considered part of a release, there is some friction there.  If you're still in yur launch phase I would not do that.  It sounds to me, its your object you migth want to do it yourself.
* Joe:  Due to how o3de is set up our only monetaization is development, training, donations.  we are a non-profit org otherwise.  We will not be selling gems and things like that.  Don't ever worry about stepping on our toes there.  The only time I will stop something is if there is a licencing issue or goes against the ethos of the foundation.
* Joe:  My understanding is not to post stuff into the foundation, but instead make it easy ot index third party gems and repos and assets.
* colinb:  The idea there was that in project manager there would be a place where you add repos, there would be a populated list curated by the release.  It would have a release list of places where you can get gems.  By clicking on one and clicking the add button you can add.
* Joe: Bryant:  We should persue both options - index and store.  Where you could pull from a list inside project manager.  Here's all the different gems available.  The other option to put the foundation page, a uri to collate all the gem and stuff.  There are issues there as well ,the foundation is neutral.  But we'd be putting ourselves in a position to maintain what we allow and disallow.  
* Joe: Having a webpage link farm was the first option we were considering
* Joe: Good luck making an interface to make that easily navigable.
* Joe:  Nobody needs the foundations permission for any of these under any condition.  If someone wants to pick it up and make the feature and hook it into O3DE, more power to them.  Just do an RFC and get it reveiwed otherwise you don't need the foundations permission or stepping on our toes or anything along those lines.  Get the feature in, this is not permission seeking.  Go talk to the sig, put it in, get it done.
* Sid_Moudgil [Amzn] - Would it not make sense for the framework AI API to be in the O3DE repo, all the actual models to be in extras.
* Joe Bryant [O3DF] - If our genAI for O3DE starts expanding for a lot we will need to have a talk to pull it out and move it to its own project.  Its not saying it can't be included, its more about how its managed, designed, people involved ,comittees that are set up for this, etc.
* Colinb: This should happen organically - put it on a repo somewhere, anywhere.  If it gets traction, moves it into extras, if its that so good we move it into the core.
* Gaian: To Joe's note, you don't want the community to have to continually support AI interfacing with their stuff, all thats been said, if its floating around thats a bohemith thats taking over, it muddies the goal.  
* Joe:  For now, lets put it wherever you want it, (Adam), Extras, or wherever.  If it gets large enough it gets its own set of maintainers, contributors, etc, for GenAI.  If it gets large enough.
* Joe:  It depends on how well it meshes with our release process.
* Adam:  We'll put it in o3de-extras, or dedicated AI repo.  We'll discuss it internally.  We are working from the POV of simulation in particular, but we are also making some effort to make sure it can be used for gaming, for example, running it on windows at all, but we are going to deliver something that is useful in gaming, its good to be able to check that.  we are not going to be building features towards gaming but we are really open to talking bout that, in terms of the general architecture and direction, we are willing ot talk to stakeholders, etc.
