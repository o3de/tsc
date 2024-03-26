# TSC Meeting - 3/26/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Danilo [Amazon]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* lemonade-dm
* Luis Sempe
* naomiwash_lf
* nick_L
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Agenda items (Ad-hoc)

### Ad-hoc topic GDC - Joe - Lot of discussion about consoles and open source
* At the Open Source round table and after discussions with Godot and W4, there are two approaches being taken
* Defold engine: one approach is extremely risky  https://docs.google.com/document/d/1BDUbr0sEppzwDSt7PXSmxpT9MSUAoFwaCeT_Co_kI2o/edit
* their foundation has taken on the task of doing the console themselves
* They have everything under restricted repo - show you are a certified developer platform
* Support xbox, sony, nintendo.  They don't have ps5 support yet but are working on it
* Risky because the NDAs for the consoles are very anti open source and also come with penalties, like for an accident are
  capable of wiping out a foundation instantly. 
* The second option, which Godot is taking, is an independent third party company that is implementing console support for them.
* The company is called W4.  Its not associated with Godot financially or business wise, they just work closely together.
* Joe spoke with them a few times, and they spoke about console support with O3DE.  We have other contributors that are working 
  On console support so we wanted to talk to them about it before we say anything about console support. 
* Joe:  opinion that the foundation should NOT persue console directly, there should be a firewall between console support and
  the foundation.  Maybe thru W4?  But we will talk to our own internal devs first.
* W4 came to our booth 3 times and one time outside the booth.  They are interested in doing console support or publishing support.
* (JOE) I want to follow up with colinb first, who is currently working on console support for O3DE.
* colinb[APMG] APMG's plan is to provide support for consoles, within reason.  Part of the overall idea is that those objects would
  be available on the APMG store and would be hidden for non-authorized devs.  
* Joe, if possible, during 2024.
* colinb[APMG] XBOX is more viable than PS4.  The renderer is not implemented for PS5 at all and I'm not a graphics engineer.
* Joe: Sid and I discussed this last night and know that a graphics engineer would need to be paired in this endeavor.

### Ad-hoc topic GDC
* Sid:  Most people had either not heard about O3DE or why O3DE is different from the others / how it differs from Godot.  A lot of them
  are trying to move off unity or unreal due to licensing changes.
* A lot of the responses are very positive.  Trying out the editor and MPS - He was trying to set up a quick scene with depth of field, 
  added a bunch of post-processes.  All of those designs and how the editor is set up makes sense to me.  He felt that O3DE was on the 
  same path as Unreal and Unity and was able to get something very quickly set and running on Multiplayer Sample (MPS).
  That was great to hear, you don't often hear personal anecdotes from people who have tried multiple engines.  Joe will cover the 
  highlights.  that was one of the big things for me.
* Joe:  I will second that, the amazing positive response across the board.  Even people who had tried it and have had difficulties installing
  said they were very happy that we exists and that we should keep trying and stabilizing and that something like O3DE needs to exist 
  in the market segment with Unreal and Unity.  A lot of features have been forced onto devs for making money for unreal and unity devs.
  They are not for ease of use of users or to help users ship games, primarily to monetize for the creators of the engines.
* Sid:  Another example is in the simulation side ,another person came by in the automotive space.
  They didn't like how unreal changed all the underlying agreements.  They wanted another engine that captures from multiple cameras, has
  lidar, etc.   They were very shocked to hear that O3DE has done so well in the robotics space.  They were interested in looking at O3DE.
* Joe:  Several government entities came by to check out O3DE for similar reasons (Simulation).  One of them stated that they are trying
  to use unreal and need something that better suits their situation.  Same as what Sid was talking about.   Amazing how many simulation
  people came through at GDC.  About 15% of people who came to the booth were not game related.
* JT: Here in town theres a lot of grief, JPL layed off 500 full time employees.  There's a massive amount of talent, I've been helping to
  find work for these people.  Its exactly people who have the expertise in the simulations.  I'll bring more info to the table by next
  SIG-OF-SIGS meeting.  Massive amount of simulation talent that is in the open market right now.  this might be a massive opportunity.
  I'll do what I can and keep in touch with joe.  Its very interesting.

* Joe: Across the board, (Feedback) was really validating.  Everyone was very positive.
* People were excited about the modularity, a lot of talk about the data driven renderer, and how they can customize it for their user base.
* A lot of things like that, people were very positive.  
* Joe: In case you are not aware, ARM has joined our discord server.  They are going to be helping (Along with AMD, Samsung, Imagination),
  are all going to be helping with related technologies.  O3DE can make games (Validation from Carbonated).  You are going to see some major
  players start to contribute back to O3DE.  
* Other people are also joining, I'll talk about them when they become more visible.
* Very large companies are willing to invest in O3DE. 
* Sid: having an actual game (Carbonated) be involved with O3DE.  Having the ability to say 2 games are coming out are huge, mobile and desktop,
  that gives a lot of reason to switch to O3DE.
* Joe:  I was talking to ARM and telling them that it would be great to get their expertise.  I showed them the press release related to carbonated
  and the conversation changed immediately to "OK how can we help?" and took it seriously.  It was similar across all phone manufacturers.
* Joe:  We need to get more games in the pipeline.  I will be talking to studios to see if anyone else will pick up projects.
* Joe:  Out of the conversations we had, the number one user need is stability.  we need to work on this.  This was the number one.  Stability
  is the top piece to everyone.  The second one was to not make breaking changes.  Making changes that break users out the gate will turn off a large part of our user base.  
* Joe: Very mixed response on larger releases vs small releases.  People like the features in large releases but not the breaking changes and instability.  But they also like smaller stability releases.  I want to err on the side of stability.
* Joe:  I might ask people as part of their RFCs to state how they will deal with deprecation if they are making a breaking change.
* Joe:  The breaking change announcement doesn't really hit the community before it breaks it.
* JT:  The OpenVDB foundation does this great.
* Joe: Please forward the details about this!

* Joe:  WebGPU is a constant request.  About 1/3rd of the people.  Sid and Steve?
* Steve: Yes
* Sid: I didn't see it as much but it was a constant request.
* Joe:  talked to adobe about Substance integration.  
* Joe:  People are happy about the houdini integration that we are working on too, studios are happy to hear about us working well with 
  commercial software despite being open source.

* Joe:  education - I spoke to many university.  I will be going to digipen and they are one of the larger game campuses.  Its really good to
  make them aware of o3de and see if we can get that into their curriculum. 
* Joe:  I talked to RIT (Rica State of Matter game).  
* Joe:  For now, I want to be really targetted about how we work with universities, I don't want to spread us too thin.

* Joe:  I spent a considerable amount of time talking to Godot / Imagination Tech. Last year there was a big fire that happened last year and
  and it was set up as an Us Vs Them (vs godot) and I had to spend a lot of time winding that back.  Open source has an uphill climb, we are
  in this together and help each other.  Each engine has things that they do better.
* Joe:  Be humble in the discussion.  We are open source, so we are disadvantaged vs unity and unreal, and they have millions to throw at their
  engine.  We need all the help we can get.  we need all the collaboration we can get.  You'll see this in the website, how I talk about O3DE.
  Its AN open source engine, not THE open source engine.
* Sid:  they are really happy there are alternatives, they do not want a monopoly!
* Godot can load any scripting language.

### Import formats.
* Joe:  Most open source projects don't have the bandwidth to support 2 different formats that serve the same thing.
* JT:   I have information from the ASWF side that is tackling USD directly.  

### GDC (more)
* Joe:  The booth was awesome and the size was perfect. I'd love ot have more demos for people to play with.  We gave away a lot of swag
  like 750 hats.
* Joe:  A random company passed by and mentioned they already used it for all their prototyping.  will followup

* Steve P:  want to talk about the logo?

### LOGO (Joe)
* Joe: We need to revisit our logo and marketting.  Our logo and marketting is boring according to booth attendees.
  we are redoing parts of the website, sizzle reel on website, will be more games focused going forward.  we'll have two seperate focuses, games and simulation.  make it obvious its a creative endeavor for creators.  just stand out more.
* Joe:  I don't want to change our logo to be completely unrecognizable to what it is right now.  Don't want ot restart from zero.  It might need more color and flair.

### Release:  JOE
* Next release in April, minor release.
* will be a point release, cherry picked additions from dev branch, pulled into the previous major release.

###  USD.
JT:  check with Josh Rainbolt.

###  naomiwash_lf:  
* looking to move to google calendar from other calendar systems.  will be reaching out to the working group leads.
* I'll give you access.  
* Joe: Also remember that as the Executive Director, please reach out to me if there's anything you need from the foundation.





