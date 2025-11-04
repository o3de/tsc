# TSC Meeting - 11/04/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L.A.
* Cheddarspice
* colinb[APMG]
* Hellaenergy (nick) [Red Hat]
* Jack420 WARDADDY
* Jan Hanca [Robotec.ai]
* Jayrulez
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Luis
* Matteo [Loherangrin]
* Naomi washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sid_MOudgil [Amzn]
* Steve P. [Amazon]

## Meeting Notes

### Announcements - none

### Discussion - RosCon - Joe
* LAst week, from 27th thru 29th was roscon, but I was in singapore before that
  due to the trip being so long to get there.
* ROScon had a few surprises from O3DE - AMD announced a project that is now
  open sourced, I found it on the robotec.ai website.  It was one of 2 demos
  in AMDs booth.  AMD is a fan of O3DE, and I had several discussions with them,
  Steve P. was with us to answer really deep technical questions so I was really
  happy he was there.  
* We were having breakfast at the hotel, and AMD researcher came to talk about
  O3DE.  It surprised me but AMD had a very impressive demo created by robotec.ai
  and it was a simulation, sim and game overlap 80%, they need graphics, scripting,
  physics, etc.  
* Takeaway from that conversation with AMD is dedicated support lines.  Open source
  projects struggle with dedicated support lines, since its at the community whim
  to answer questions like that.  We can't generally do things like pay for support
  or things like that.  I will look for IF thats possible for a non profit org.
* This is why companies like redhat exist.  Its a dedicated, commercial company,
  whos job it is tosupport specific open source projects.  A person, or company
  at 2am thats running into a problem and will know that someone will be there to
  solve critical problems or provide support.  I desperately need to look into this,
  and large companies are adopting O3DE a lot.
* Particularly people who represent or work at redhat who have experience in this
  area.
* That was an awesome thing to have happen.  There are several socials going out
  about o3de at roscon, particularly at AMDs booth.  There were a lot of smaller
  projects that were using O3DE.  Lots of companies using O3DE and not talking
  about it.
* Told them to join the discord, we have a very helpful community, you will see
  an influx of people coming in.  Now that AMD is advertising the fact that they
  are using O3DE.  They launched this new Ryzers AI and created a packaging for
  o3de.  That was the highlight of the conf, that we are featured by AMD
* O3DE is "The only open source 3d engine with a good renderer that is truly
  open source.  The other vendors have vendor lock"
* Jan Hanca:  We also had that demo on multiple other occasions, in our booth.
* Joe:  In this conf, it was in AMD's booth itself.
* Sid:  AMD Builds a lot of tech in open source, did you talk to them about
  integrating any of their open source tech into o3de.  
* Joe:  I really wanna remove the black box around GI and raytracing, they are going
  to point me to the people who can help with that.  they are keen on helping me
  connect to the right people to get that done.  We'll have the gaming an sim side
  pro o3de.  I told them, "we can't put them all this in on our own, we need help
  from AMD engineers." and they said it should be doable.  I did talk to them about
  trying to remove cuda shaders from raytracing and adding fsr and GI.
* Joe:  This doesn't mean we'll remove the access to the nvidia shaders, since it 
  would be faster.  We're trying to make the open source version for AMD the default.
* Sid:  The shaders aren't necessarily faster on nvidia.  Its just the only tech
  available.  It shoudl be phrased as the "integrate your GI solution into the 
  engine an we'll probably make it default".
* Joe: For an open source project, it behooves us for our defaults to be open source.

### Discussion - Intrinsic - Joe
* Joe: I talked about google as well about O3DE and sims.
* Google owns intrinsic and intrinsic is gazebo.
* It was a good conversation, and the renderer in o3de is heads and tails above
  any other open source renderers including gazebo.  In general, there might be some
  collaborating happening between intrinsic and o3de.  We'll see.
* There's also a medical company using O3DE for sim skin graphs, etc.  we were 
  mentioned in "best of" simulators available
* I ran into kimberly (twitch channel and blog about o3de and drones).  Also, she
  did a best of with o3de coming out on top.
* In general, O3DE was very positive, but steve and I were going thru all the booths,
  and we went by one booth and as soon as we found out we were from o3de we almsot
  got kicked out the booth.  Its because we're giving sim companies a lot of
  competition for their products.  They're dealing with a lot flak from doing that,
  having us from O3DE pop by rubs salt in that wound a bit.  It was kinda funny.
* The engineers were fine, it was the sales guy that was a bit of an interesting
  person.
* Overall every year we see more and more talk about O3DE At every conf we go to.
  I will be canvassing the community about this, me going there to O3DE, but having
  someone with me, like, but having someone else there for games, I will try to
  drag another technical expert with me, we will generaly pay for hotel and airfare.
  Its an opportunity for people to be exposed to these events, network for jobs, and
  it helps me and O3DE out.  My knowlege isn't as deep, so having someone there that
  can speak deeper into the tech itself, when people asks those super deep questions,
  having Steve there was a huge help.  Its a lot more enjoyable with a 2nd person
  and a second set of eyes and opinion as well. 
* Lots of positive surprises across the board.  Robotec.ai gave a talk about o3de.
* I do research every week about mentions of o3de across the internet.
* Week before I saw some job postings for intrinsic, and int he job posting it said,
  recommended skills:  experience with O3DE.

* Unrelated: O3DE has been our best o3de download months, period.  The release was 
  less than half the month but we still have the by far best month period, in 
  downloads.  Curious about november, december.  O3DE is making a lot of noise, 
  we are getting a lot of notice, and we have some large companies who are
  seriously coming to the table now about o3de.

* Questions:
* Colinb: AMD Partner?
* joe:  Yes, we need to answer the support question
* Joe: Anyone looking at building a commercial support for O3DE, that needs to happen
  right now.
* colinb:  APMG does that, but its super expensive.
* Hellaenergy:  any feedback about latest release?
* Joe:  No.  Just that engineers really love it.  They wont' talk about releases,
  specific, they'll talk about trends.  like "its getting more stable, etc"
* Joe: Another thing mentioned a lot:  Gaussian splats.  I'll put that on the
  roadmap for 2026.  Not just in a sim space, but in game space / content creation.
  It was mentioned often for o3de.

* Steve:  Runnign the demo drained my battery really quick.
* Joe: I was running the editor and battery lasted like 20min.
* Joe: Mentioning that because the editor runs at the fastest possible rate, it drains battery very fast if you're using a laptop.  
* Joe: It should easily link the editor to vsync or something so its not freerunning and obliterating batteries.

* Colinb: AMD say anything about looking at O3DE at an alternative to omniverse.
* Joe: I can't go into details but good line of thinking.
* Joe: They made it clear we are the only viable open source project with the
  quality they need for sim out there.
* Steve: It was also mentioned that o3de was way more performant than omniverse.
* Joe: and we're not vendor locked.  Thats a big one for people, you can use
  whatever hardware you want for your sim.  Especially given quality of renderer.
* Joe: Even talking with intrinsic/gazebo, it was all about the renderer.
* Joe: People would ask the question about the demo robotec.ai has done for AMD,
  they'd ask if it was "Isaac sim".  Thats kind of a compliment for o3de, it has
  a very solid renderer with it, but its vendor locked, etc.  the fact that 
  people are confusing us with it is a huge compliment.

* Joe: A lot of people might think "who cares about sim, I only care about games"
* But every optimization we do on the sim side, directly impacts (positivley) the 
  game side as well, since 80% of the stuff is shared between games and sim. 
  Big companies like AMD can help improve render quality, etc, which affects
  everyone that uses O3DE.
* https://www.robotec.ai/blog/robotics/advancing-agentic-ai-with-amd-liquid

### Discussion - Jolt - Cheddarspice
* I've been doing physics with replicated input with jolt due to cross-platform
  detmination.  As we've been talking about upgrading physx to the latest version
  and the challenges involved 
* Joe:  How difficult has it been to get Jolt into O3DE?
* Cheddarspice: The hardest part is I only just started c++ in about 3 years.
  Its been an uphill battle with the build system and everything.  inside, 
  jolt is very well designed and its been very easy.  
* One of the things I ran onto was the difference in the phyics system.  In
  physx for example you can set the rest offset per shape or body, but in jolt
  but those are not configurable things, like, its a global setting.
* Lots of physics has a lot of duplicated cruft, and theres like a thousand lines
  of the same code in each collider.  What features I can replicate, what things
  there are no analog for has been the biggest challenge.
* I think, what I'm hoping before Christmas time I can have static and dynamic
  rigid bodies, a bunch of squeares as a proof of concept.
* Joe: This sounds like a great blog topic.  If you're interested to create
  a blog, I can connect you with Naomi and our marketing people and because
  this can guide people in the future.
* Joe: Lessons learned, etc.  Basically to help others who are thinking about
  replacing a feature or physics engine or etc.  
* Cheddarspice:  Part of me is just like "man I wish I didn't start it, but
  maybe if I do finish it, maybe I do contact havok and see if they would like
  me to try to do it for them too.".
* Joe: I am in contact with them and we can get in contact with them if you
  feel comfortable.

* Joe:  The main reasons we used physx4 + physx5 was platform support.

* Cheddarspice. there have been a few particular pain points (Wth jolt)
* An example, u64 collision layers and groups (collison filtering). 
  Optionally ou can change it to a u32 as cmake flag.  They have a separate
  broad phase filter, but really tough but fun challenge in bit manipulation.
* Reece: I was thinking that the engine would have a standard layer, and have
  a standard.
* Reece: Having a generic audio component or bus, or miniaudio has its own bus,
  own component, no generic way of playing.
* Reece: For miniaudio, for sig-graphics-audio channel, because of the legacy
  of the audio layer, its still hooked into CSystem (CrySystem) after all the
  system components.  It breaks my logic and a lot of my code depends on a
  labsound initializing we expect it to be available.
* Maybe instead of breaking WWISE, we make a new layer that slowly over time
  get rid of it, and maybe WWISE updates to it.  Some system component with
  the same functionality.
* Something I want for labsound/miniaudio/ATL stuff can be broken up for
  a basic / more advanced layer.
* colinb[APMG] it lends itself to some systems and not others.  Phyics, makes
  sense.  But if you try to apply it to a rendering.

