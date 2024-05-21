# TSC Meeting - 5/21/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Guthrie [Amazon]
* Joe Bryant [O3DF]
* Luis Sempé
* MichaelP
* Naomi Wawshington
* Nick_L
* null [meta]
* Sid_Moudgil [Amzn]
* thoraxe (Erik) [Red Hat]

## Agenda items
https://github.com/o3de/tsc/issues/125

### Agenda Item: Erik and Joe discuss O3DE import public asset
* Erik - It had been a while since I had played with O3DE and joe had mentioned that there had been a lot
  of changes to the getting started experience.  We had a day of learning where we did a lot of doing whatever.
  * I did the install, and that was great now.  It immediately fell apart with respect to grabbing 3d assets.
  * I've used a godot asset many times, imports great, everything works, the first thing was logical to do was to put
  the asset in o3de's asset browser area and it immediately crashed to desktop.  Never crash to desktop.
  *  Never cause the user to spelunk in log files.
  * When we did that, the entity was better, but I was able to run into all these QoL problems.  
  * The preview of it is the a statically pulled image.  You can't preview the import. 
  * There were issues with pulling the texture file even when its right next to it.
  * The experience was terrible from the "asset store" situation. 
  * If I was a triple A creating assets specifically for O3DE, it would probably be okay to have an advisor
    explaining exactly how to pull it in, but if I was an indie using assets from an asset store it was awful.
* Erik - I tried both related to texture path finding and not anything else.  There is a sea of test content that we
  could use.
* Nick:  The current system uses the free Asset Importer (ASSIMP) to load assets and parse them into an independent scene format.  Then it runs a bunch of hardcoded C++ heuristics on them.  Then it calls an optional python script.  There's not enough python hooks for it to really be viable.
* Joe:   For Robotics we pulled in 2 assets that everyones using and so used it
* Joe:   I'd like someone to pick 2 major repos and collections and say "hey these should be our test cases"
* colinb[APMG] : I was part of ameeting of another foundation org that was trying to have a standardized set of art
  that engines can validate against.
* Joe:  ASWF has a project to establish a standard too.
* Joe:  For now, what is are some good test repos, collections we can pull from. Start smaller, identify the repos,
  that's our first step.  
    * As a separate action how much work do we put in for this other foundation to establish standards.
    * A couple at GDC was talking about standards, for gaming.  
    * Let me know that info (colinb) I don't want us conflating the 2.
* colinb:  JT is one who told me about it.
* Joe:  Likely the same ASWF and likely about USD.  Its a WG from ASWF to get a whole bunch of large game companies all
  trying to figure out how to standardize on USD and still get the things they need to get done.
* colinb: Maybe we can put a few assets in a couple repos, seperate repo maybe, and put one of each type or make them canonical.
* Joe:  I don't want us copying assets over from these collections though, I want to grab the repo, or say we test against these collections and say that it imports and don't carry copies or duplicates.
* Joe:  You pointed out to me a collection thats saying "these assets from this site is commonly used, they tend to be quality assets", etc.  
* erik: The challenge is the license of the asset.  None of the assets are CC on unity store for example.  the challenge is finding the asset more than finding the marketplace.
* Joe:  If we have to go with a list of assets thats fine, but for example robotics AWS robotics we said there was a huge repo and we said 90% of those needed to work.
* erik:  Random marketing hat thought, we might be able ot get a marketplace to sponsor the 3d community and give us assets that would normally cost money.
* Sid:  How do we actually address the crash when we find it?  Possible strategies, labelling filtering, the filter needs to iterate on, sigs, TSC meetings, until you push these issues that need to be fixed, nobody is really going to be fixing them.  I as a rendering sig can push other engineers to address them.
* Joe:  I'll mention in sig-content that we had this discussion in this TSC meeting
* Luis Sempé: I'm the chair of the SIG-content.
* erik: A customer will gladly crawl over broken glass if they know that the end of the project that the thing that they want will eventually happen.  Its not the end goal, but it will unblock a lot of people that really want to use this engine, right now its a mystery to make it work.
* Joe:  showing actionable errors.
* Nick: https://docs.o3de.org/docs/user-guide/assets/scene-settings/
* Sid:  Keep pinging the discord with these issues as it goes along.  We'll otherwise create issues and they will never be seen again.  They get lost otherwise.

### Agenda Item: Stabilization to dev cherrypick
* Joe:  a lot of fixes go into stabilization and we need to make sure those changes go back into dev.
   * What we have done in the past is that ask for volunteers to do a weekly integration from stabilization to dev, so that prevented people from having to do giant complicated integrations at the end of a 2-3 month stabilization, but what happens is as stabilization goes on and bugfixes are made, dev continues moving forward and they diverge so much, it becomes extremely complicated because things are very different in dev compared to stabilization at that time.  By doing a frequent integration frmo stabilization to development it prevents the divergence from getting so large that it complicates the integration.  USually its really quick, one or 2 minor issues, get your approvals and integrate.
* Joe:  About 95% of the stuff go in, 9/10 go in as is, and one integration for an entire stabilization pass has a complication for feature divergence.
  * With that, what I will do, is go ahead and create a document to allow people to sign up to volunteer to do an integration pass.  We'll do it once every 2 weeks is a good cadence, and I don't think enough is going to build up.
  * (Sid will send the steps to Joe.)
  * What do you think the best place is for this?  An issue?  A doc?
  * Nick: An issue, you'll need one for every release...
* Joe: You and I and any of the sig chairs, help evangelize.

* Joe: All our marketing and communication will always have a CTA going forward.  We should be calling out contributors github names.
