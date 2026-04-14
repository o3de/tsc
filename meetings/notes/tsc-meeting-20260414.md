# TSC Meeting - 4/14/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* Atmosaero
* ChristianHinkle
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sean-RP1
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

### Announcement - Naomi about O3DF
* Membership funding is low
* Governing board realized that we need to keep the most important areas operational, to keep O3DE alive.
* That is largely Infra.  With everything going on PMO and Marketing have been removed from the foundation side of things.
* We are moving to a community-led project.  This is common in open source.
* This is not necessarily permanent, if funds come in we can ramp up again.
* This project has largely been community run since I've been here for 3 years now, the largest issue is going to be marketing,
  but we can still do marketing - its more on a volunteer basis rather than LF Marketing team.
* Naomi - I will no longer be in the Connect Meetings, its been hard in 6 months to get people to talk in those.  It will still
  Sit in the calendar, people can show up and talk.  More demo driven.  Larger community updates, easily assessed to the community,
  I'll move it to a discord channel.
* Naomi - Marketting committe meeting, the governing board made it public, we are going to move that to a discord channel and do
  push reminders to hope people join more.
* colinb: Who is the director or taking the lead?
* Naomi - Todd Moore has been working on this since Joe Left.  We're trying to close a few in the pipeline, but it hasn't happened
  yet.  If things come in he'll pick it up.  We also used to have membership support.  If you all do know members that are
  interested, still point them out, we don't have someone super dedicated moving forward.
* Hellaenergy - Do we know when new members come in and who they are?
* Naomi - We still have members and will still announce to the community when new members come in.  we'll be sure to communicate
  it to the community.  There are tiered ways.  You all being the main maintainers and TSC members, we give you all in-depth,
  and we'll send another email to the larger community.  I also have a FAQ that I have on the website, and we can point there.
* Naomi - we still have code being contributed, contributors, and we are just focusing the remaining funds on the infrastructure.
* Hellaenergy - Where did you contribute before, and how can we take over?
* Naomi - Scheduling, you were already self-sufficient.  I was more involved in the comittees.
* Hellaenergy - you helped with the releases?
* Naomi:  Let me do another doc, that highlights those pieces, and we'll talk about the github access and so on, so I'm not
  a bottlneck moving forward.
* Nick_L Q: The website consists of both content from o3de.org github but also some non-o3de.org content.  Same with binaries.  Do
  we have the necessary access tokens in the necessary hands to update that site as well as binaries?
* Naomi:  We can give them keys.  We could submit a ticket, or get the website update with the ticket.
* Hellaenergy - how about the marketing aspects of things?  That Crystal was doing.  Someone from Red Hat *might* pick that up,
  but what in the meantime?
* Naomi:  Marketing is fully pulled off, they are not even popping in.  I wouldn't be comfortable, saying what the tone should be.
  I'm also supposed to be rolling off.   Let me pause on that, we need to find someone in the community to hand the LinkedIn keys
  to.  Don't trust me with any kind of keys to social media, I am not a marketing person.
* colinb[APMG] - Do we still have access to LF Legal?
* Naomi:  This project is still part of LF, and still has access to all the resources LF projects have access to.  Its the operational,
  project specific costs.  Access to legal, discord server, groups.io, etc is not going away.  Its just LF dedicated staff, that is
  dedicated directly to the project like Marketing.
* Hellaenergy - How do we know what the board is doing?
* Naomi:  The board is your people - Nick_L, Sid, Adam (Robotec).
* Naomi:  Project is healthy and active, you can see LFX.
* Timeline on additional Announcements?  - I wanted to send that email to you all, have space and forum to ask questions, and then
  I want to adjust market community meetings -> discord, along with o3de connect -> discord, and then send an additional email 
  with fewer details to the broader community and will be around to field questions.
* JT: Some projects are preferred to be run by the community directly.
* JT: Growing the community through a user group movement, I expect this to explode at siggraph.  I expect the work with the USD
  work and collective project.  I expect it to jump, and I've done some substantial work that will be coming out this and next release
  and will be generating external docs outside the project that want to develop tutorials and stuff.
* Some people like it when LF is a bit more hands off, and the community has more agency.
* colinb[APMG] - I'm fairly comfortable where we're going, I don't see it as a main issue, the only issue is I see a flywheel effect
  where when there's someone actively trying to get funds from companies.  We need to do something, even if its community driven,
  to keep that flywheel moving, and try to get more funds from corporate sponsors.
* Naomi:  We will still chase down any leads you find!


### Discussion Topic - ECS and O3DE (nick)
* (Nick describes ECS in O3de)
* JT [SCB_GameDesign] - How does it scale?
* Nick:  It probably scales worse than a true ECS.
* colinb:  Its probably the flexibility - you can start with the simpler EC version, and then if you find yuoruself in a situation
  where you have 200,000 entities, then maybe you consider its time to switch it over to using a bespoke system for it.

### JT:  Atom is a system? - Notes on Lua
* One of the super powers is the render pipeline, and the fact that you can change the render passes, you take one out, it still
works.  You can do things externally and bring them back in, and you mentioned some of the render passes, in its data centric
model, and is held together by Lua.
* TinyECS was implemented in Mozilla Hubs, and moved to a social platforms.
* Sid: With render pipelines, you can build them via JSON, or Code.  There is no Lua involved in building the render pipeline.
* Lua is used when managing materials and tagging datasets and data and how it interacts with pipeline.
* There is docs about how to build render pipelines, and videos.
* You can use Lua in the material pipeline to help tag specific shaders with the right meshes in the right places.  The render
  pipeline is JSON files mixed with some Code.  All getting tagged together.  Its data driven, you can build the whole thing
  with data, no code involved, or a mix of both.

### Sean-RP1:  CEO and founder of RP1
* We are building the world's first metaverse browser, building the evolution of chrome for AR glasses and such.
* We are looking to use the atom renderer as a component of the metaverse browser.  We are using the renderer, and someone
  can build any kind of game or website using the standard.
* We are using a lot of standards from the khronos group, fully involved with Inari.  Anari is render agnostic, and 
  anyone would be able to take the core and make a competing browser.



