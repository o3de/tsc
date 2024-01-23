# TSC Meeting - 1/23/2024 

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* nick_l
* Joe Bryant [Amazon]
* Steve P [Amazon]
* Adam Dabrowski [Robotec.AI]
* RoddieKieley [Red Hat]
* Tobias Alexander Franke [Huawei]
* null
* Sid_Moudgil [Amzn]
* Michal Pelka
* tkothadev [Amazon]

## Agenda items

### Agenda Item: Joe Bryant - RFC from Robotec.AI
* Link to the RFC is here: https://github.com/o3de/sig-simulation/issues/86
* Adam:  Link is also in sig-all
* Adam:  The new feature set helps open 3d engine devs to utilize modern AI in games and simulations.
* Adam:  I'm not sure how long the Generative AI would last.
* Adam:  Its for using AI generated robots, simulation, entities, etc.  The gem acts as an enabler for AI but does not itself include any actual AI * feature, and we plan to follow up with other gems that will utilize it.
* Adam:  Its meant to be vendor independent, but include one open source (For example Mixtral), to be a moving target for us to hit, and have a tool that is modular and easy to replace, upgrade, and configure.
* Adam:  Part of this gem is the ability to interface with O3DE with AI, such as creating new entities and components, one of the applications that I see could be achievable with our current state of art is assistance in creation of levels, with existing asset, such as smartly randomized layouts, which is not the same as random, because the arrangement also has reasonable placement.  AI CAlling O3DE interfaces, calling thru structured / JSON format and interact with o3de.  
* Adam:  AI will need documentation much like humans do to understand what this API does.  But also expanding modalities to allow the AI Assistant to see  the viewport and the environment.
* Adam:  (The Link Contains) API description, references.
* Adam:  It also has open questions.

#### Questions?

* Joe Bryant [Amazon]: When does this RFC Close?
   * A date will be added, likely a month
* RoddieKieley [Red Hat] - is this for LLMS specificially?  Should the name be AI core gem? or something closer to LLMs.
* Adam:  When you look at the history of the field, some of the terms that were used prevalently are not used anymore, and LLMs is not a term that is accurate anymore.  It will be hard to name but will be referred to AI.  I am open to naming?
* Null:  might be LLM.  
* GenAI Core Gem, LLM Core Gem.
* Nick:  Runtime, Developer, both?
* Adam:  Its for both - runtime, as well as developer -  for example, in game, realistic characters, for robotics, etc.  Content creation collaborative is also for the Edit time.

* Null: local GPU framework you proposed, is it far future?
* Adam: More and more providers are exploring this, we are hosting Mixtral here and playing with it, and Llama.  How people choose vendor and model is a complex issue but should not be limited by this gem.
* Null:  Proposing actually bringing in google's tensor library or pytorch?
* Adam:  We are using Llama.  We implemented one example . We should include one example.
* Sid_Moudgil:  It will be interesting to see how the device is shared between O3DE-RHI and the GPU library you are integrating with, and how it is shared.  Maybe its possible?  There will be some complexity there.  
* Adam:  For local it could mean local machine, could mean local network.  We are currently testing local network - internet enabled model.  
* null:  Not same box?
* Adam:  Local on-prem, not local on box.  I see in the future SLLAM or other small applications / footprints.  Here is a conflict for resources to run on the same machine.  
* null:  Be clear about local device / local network.  You can use your same exact websocket interface.  Whereas local on device unlocks extremely low latency interactions but has larger technical implications.
* Sid_Moudgil:  It would require a lot more fleshing out about how the device is managed.  Is it a separate device?  They have API to do large language models on the drivers, but RHI does not expose it (it could, but that's a different conversation.).

* Null:  You might be able to generate the assets directly (xml, json) without behavior context.
* Adam:  Existing reflections don't have a lot of documentation. There are some arguments for a custom approach, but based on existing structure.
* Null:  Depending on context window side you might want to dump the API with minimal documentation.  
* Adam:  All good comments to add to the document!

(A technical discussion about prompts and prompt optimizers began here)

* Adam: We will start with the core features here.  This will require constant updates to keep up to date with the dynamic field.

* null: Talking about multi-modal models in the future . The visual multi-modal models are really far behind the audio ones.  
* Nick: We have MiniAudio now and a microphone gem.
* Joe Bryant:  Be wary of expanding the gem's purpose too far initially.  Let's come up with the use cases that this can cover initially and then architect it so that the framework can be added to over time.  If we bite off too much it could make it hard to implement or delayed.  So get this thing up there and maybe its not as full featured but at least there's something up there, and then expanding upon it.
* Adam:  Agree - when additional modalities become common, maybe that will also become a part of the gem.  But separate decision.  For now, modalities.
* Adam:  To paint a bigger picture I painted futures that won't be a part of this gem.
* Sid:  similar to the XR gem, but it can be extended by openxr or other people.  

### Ad-hoc:  Joe Bryant 

Joe:
* Noticed over last couple weeks that graphics PRs have been submitted but had some serious negative concequences and not things you would find in a code review.  Whats the best way to approach this so that contributors can know that this PR has a negative side effect?  Everyones currently testing against the graphics test, but it doesn't cover the use cases, especially shaders, etc.  
* Maybe test against the multiplayer test?  
* We've been able to fix and we've reached out to submitters to fix the PRs and negative side effect, but its to the point where these PRs are submitted because you can't build or can't find shaders or something like that, or serializtion changes so you can't load things that you already made so you can't serialize the assets anymore.  
* We've only just started thinking about it
* I'm open to any ideas.
* Sid:  ongoing conversation of 4 years of Atom's development. AtomSampleViewer contains all the screenshot testing an atom developer would be able to use.  Downside it is that it takes a lot of maint., tried to move some of it to AutomatedTesting, it needs to have very little friction points.  it makes sense to automated testing, it ships with core of the engine, its small enough to not take a day to setup, on platforms other than windows as well, and test within it.  we had ported the python framework, and the idea was that you would build a level and all the screenshot stuff would exist in that level and all the golden screenshot stuff would be in there .   But it never finished and nobody ended up using it.
* Joe:  Serialize/deserialize needs to be added you need to check if those are backwards compat with the existing art.  You have to give the audience 6 months of updates with impactful change if you break serializers and your stuff won't work anymore.  Preferred option is that you have a deprecation pass so that you can load the new and old serialization.  For x amount of time both formats are valid.  We can't be breaking serialization out from under people and force deprecating their work.
* Nick:  Could we just use a basic render test level?
* Sid:  Automatedtesting levels/AtomScreenshotTest.  A level, you go in, etc.  Two levels with this vision in mind.
* Joe:   Just run thru the level and see lighting and particle effcts and so on, just lots of stuff down the line.
* Sid:  Add everything to one level?
* Joe:  Create a plan for how this should be tackled.  Putting this out to the community and asking 'what do you think?' etc.  There should be something that lets you just quickly use to accidentally prevent problems.  Accidents will happen but this will minimize number of times.  I will take an action item to work on a plan.
* Tobias:  We have set up some internal testing, but I haven't looked at it.

