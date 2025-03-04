# TSC Meeting - 03/04/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* 
* Mike Chang [Amazon]
* Nick_l
* null [meta]
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Joe
* Joe is at a conference tomorrow thru Sunday. SCALEX (Linux Conference in Pasadena)

### Announcement - Joe
* Stabilization for 2505 has been created.  Note that Robotec.AI (Jan etc) have brought up issues with the process
* Mike and I are working on resolving as many of those as we can for future releases.
* Those involve number of reviews required into a Stab or Pt release when we do a PR
* There's an issue with stabilization AR which targets dev, which causes all sorts of issues, o3de-extras and o3de
* Mike Chang - Do we even need to build like this?  
*    Projects and gems don't really have enough tests, how do we actually care about this or test this?
* Nick:  Could they not use their own project (from extras or other?) and use the nightly installer version or something?
* Robotec.AI and Meta both contribute to o3de-extras, none of this is a done deal, we're thinking fo this, as ExecDir, I don't mandate 
  anything - ultimately its up to the sigs and the TSC to enact whatever solution they think is best.  I'll set guidelines, user, quality
  of life, etc.  Whatever tech solution is what we're going to go with.
* Primary goal is to improve the QoL of anyone who contributes to sig-sim, and the quantity of updates is high.  Keep Robotec interested
  and feeling like they can keep contributing as a daily work thing rather than a thing they dread.
* Jan:  The important part and most severe part is that there are no tests for simulation gems at all.  we don't have a test project
  and the tests are not executed in AR, and so the whole thing is like making a change in a Readme.txt and having it build the entire
  AR which builds all the tests of O3DE and runs everything.
* Joe: As an initial solution, maybe we disable it initially and then figure out what/how we can do a long term plan?
* Jan: Maybe github actions switch to, once it runs smoothly, we can port all our tests we have internally into that.
* Joe: When is ETA for github actions?
* Mike: End of this Q.
* Joe: Another thought, extras contains a lot of robotics stuff and AR/VR/XR.  I like repos personally to have a single purpose, so that
  people know what repo they go to for certain things.  First thought / split AR/VR/XR into its own repo?  Second, very long term, 
  renaming o3de-extras to be o3de-robotics or something along those lines.  Its difficult to find things for O3DE.  O3de-extras doesn't make
  sense for new users who are looking for robotics.
* Sid_Moudgil: Test for O3DE extras was added for XR support.  Why these tests were there was to make sure all the OpenXR / Vk stuff.
  The idea was there that they could all be tested with automated testing framework.
* Does meta attend TSC?  Sid: they attent sig-graphics.
* null:  We have more than XR and robotics in there.  Follow through to figure out whats in there, and random stuff.
* null:  Previously what we said was anything not required to boot the engine up should be in extras, and so its growing.
* null:  One more loop to jump thru - the direction we're heading is a healthy one, wehre we have multiple different repos you'd sync to and configure your engine for robotics/sim purposes, games repo, ar/vr repo, for each use cases.   The problem is you're going to have gems that common across all those aspects.  Not required to boot the engine, now we've introduced a heirarchy, so thats also going to be require some forethought.
* Sid_Moudgil:  From a GFX perspective, there are GFX features like meshlet or harmonics that are in the core repo. You create a new repo, o3de-render or whatever.  All the core features will be there.  But everything tier 2 and so on can be in this repo.  It shows up in the projectmanager, but you can always swap them or pull them in or out.
* Joe:  Project manager can be prepopulated with repos, so that they show up and you can choose them and grab them.

### Announcement - Guillaume [CI]
- https://github.com/o3de/sig-content/issues/151 (Script Canvas Breakpoint Support)
- https://github.com/o3de/sig-docs-community/issues/142 (Showcase page revamp)
* lsemp3d - Script Canvas is straightforward, standalone viewport involved pulling atom into it.

### Discussion - Joe - Reorg Discord
* Joe:  I take part in a monthly marketing comittee meeting.  one of the benefits of joining O3DE is that you get access to this meeting.
* We have decided to open that meeting.  At the last meeting, (last thurs) a lot of time was spent on how new users struggle to get both
  feet into o3de quickly.  Some of it is dealing with docs pages, which some people have ideas about, but the biggest thing brought up
  is how its difficult to find things in discord.  
* Right now, we dont' really have channels that point at specific topics about O3DE.   Suppose I'm a new user I'm interested in graphics for
  o3de.  Right now, we have sig-graphics that people could go into, but that sig usually talks about technical implementaiton details, RFC, 
  that kind of thing.  Same for all the sigs.  
* One of the ideas proposed was lets clean up and make 1 support channel, they can go to get support if they're not sure what to do, the second
  piece is creating channels around topics like general graphics, general audio, general scripting.  Same thing for networking/cloud/etc.
* Let's think about how our discord could be new user friendly.  In the beginning it was targetting big studios with large teams that are fairly
  technical.  O3DE has obviously grown and we're getting a larger audience and a lot of people who are coming in with a unreal or unity mindset,
  and less want to dive into the code to understand.  We have to pivot a little to help those new users find what they need to find.
* Thougts?  Primary person is a marketing director at red hat, they have the chops.
* null:  My bias would be to make 2 different discords. 
* Joe: The concern is fragmenting our userbase.  But it is an idea, a good idea, what we're going to need to do is take all these ideas and figure
  out what the pros and cons are, and the sigs, and figure out, is having a 2nd discord to maintain, does it water our community down.
* Joe:  Something that Godot does really well is several different entry points for new users / contributors / etc.  They ahve a very large
  community problem because they don't ahve enough godot sanctioned mods.  They have different owners that are not affiliates.
* Joe:  one problem with discord is its really difficult to find.
* JT [ SCB_GameDesign] - The reason discord has changed a lot of this, thats part of why this change has been made.  This is a very robust system
  that has been used for very large conferences and tools.
* Joe:  While I'm in pasedena maybe just the 2 of us could talk!  I want to strategize about THIS.  JT you have a lot of experience in larger open
  source projects and their communities.

### Joe - Commercial software used for demos / screenshots
* Open Source software foundations have been successfully sued for commercial software usage in their demos and things.
* null: Please get legal involved in these
* Joe: When I talk with Mike Dolan (our legal) and see what he says in terms of nuances, we'll get that written up.
* PRetty sure mikes going to say "Don't do it"
* Nick: Is this like, using software that has a watermark or something?
* E.g. using screenshots from some Commercial website as an example when suggesting new design for O3DE website.
* E.g. suggesting changes or screenshots from houdini or something saying "we should do it like this".
* For now, we're going to forbid it, but maybe we can get some nuances from Mike.
* Same thing goes for automotive things (Don't make a specific vehicle)
* Other examples :  Hollywood sign, speciifc buildings, specific vehicles, specific characters.


O3DE is about users and contributors, and when the foundation comes in and says "we have ideas about this", its all of you that determine direction.
Contributors and users are what make the wheels turn and determine the final direction of O3DE.  Whan I or Naomi is presenting something we will
make it clear when its a (legal) requirement.  Other than that, all of you are the primary leaders and determine the direction of O3DE.
