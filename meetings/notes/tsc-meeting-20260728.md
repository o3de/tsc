# TSC Meeting - 7/28/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* colinb[APMG]
* hellaenergy (Nick) [Red Hat]
* hex
* Jan Hanca [Robotec.ai]
* jayrulez
* JT [SCB_GameDesign]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* std::vector<☠> P-Rose
* Steve P [Amazon]
* Tamashiko

### Announcement - SIG Release proposing a stabilization cutoff
* Last one was at the end of july, and we are at the end of july.
* I'll be posting in the SIG-release channel for more detail.
* JT - Figure out the multiplayer template overwrite issue.

### Feedback on Siggraph - JT
* Stopped multiple times for stickers for ODIE
* I did the ASWF USD working group workshop talk.
* Explained of splash screen project together, collective.  Backstory about how it was started on a piece of paper, mascot.
* I'll make a written report on the go for the meeting, I've made some good connections with the USD community and other devs.  O3DE got a lot
  more traction at siggraph, and a lot of people are taking a closer look.
* I worked with blender people, mac people.
* Siggraph went well for O3DE.  People were stopping me about the hat.  The hat worked!
* ColinB: I also went to the SIGGRAPH.  I was really impressed with the ASWF, and could benefit from the integration of a lot of that stuff into
  the engine.  
* JT: I met with the TSC chair of OpenTimelineIO, and talked about plans, tooling, virtual production, OpenTrackIO, OpenLensIO.  Colin got to meet
  some of the people I've been collaborating with.  I put them on notice that we're coming and intend to integrate into O3DE more deeply.

### Arbiter has a PR that removes the IPlugin Cry plugin system

### colinb LYSHINE replacement (SHINE)
* Arbiter suggested we broke it up into prs
* We suggested we put it into a branch?
* The breakdown we put it into those 2 PRS, its a couple thousand files, a large number of files are just copied from one place to another.
* SHINE is just a copy to lyshine.
* If an object is on deprecation path, should we accept PRs that involves fixing it.
* Shine has a full migration path from lyshine to shine

### Discussion 
* Style Sheets optimization by nick
* Discussion in the discord - thread about Qt6 - but the summary is that style sheets are very slow to evaluate, and happen whenever the styles
  on a widget change.  This occurs when you reparent a widget to nullptr, or move it between places in the hierarchy, such as `setParent(nullptr)`
  to put it in a widget pool and then subsequently take it out of that pool.

### Discussion - deprecation system
* notes on Qt deprecation system

### Discussion - Jan Hanca 
* There was an information about upcoming release, feature lock for development branch * split of branch
* Is there a point release coming?
* There are so far, a release, o3de-extras alongside the engine.  Since there is no O3DE release before roscon, I would love to consider a point
  release for O3DE-extras, so we can release some bugfixes before the ROSCon for the newest version of ros.
* JT: If we have some sort of comms policy where normally we'd come with a release / point release or docs where people can see that we've bumped it
  up.
* Next Sig Release is half an hour after this ends.  Nick and Jan to attend.
* JT and I were discussing how to move the blog to github and hugo.  So we could do a PR to update the blog.
* We shared the work we did with the community
* Since 26.05 is a step forward for us, we use it actively, we actively found a few things that could be improved.
* Before we switch with our customers to 26.10 next.

### discussion - colinb - Schema 2.0 is getting close
* https://github.com/orgs/accesspointmg/repositories
* https://github.com/accesspointmg/org.o3de.repo.o3de/blob/development/Engines/o3de/rfc/o3de-2.0.0.md
* Object system is working
* O3DE - Pilot updated and working
* "Chickenation" of the repos working (Colinb's word)
* 120 repos, all of the objects that are inside the engine, all the objects inside extras, all chickenated out into their own repos.
* Maintain an upward connection to the repo o3de/o3de and when they make changes, I can filter the changes down into the objects.  We the nature of this
  is that we can restructure the engine any which way we want, whatever makes sense.
* Reverse domain naming
* o3de-pilot: https://github.com/accesspointmg/o3de-pilot
* Intended to be the downloadable, each other part is published individually, if you were to put it in a snap package or apt, it would be the pilot.
  You'd run that (Python/QT6 application and looks the same on everything).  Has the AI integration in it, terminal integration in it, you can run it
  like vscode, typing commands, etc.  You can see the AI or UI typing the commands in.
* I've split the platforms out of the objects into overlays.
* https://github.com/accesspointmg/o3de-pilot is the key repo.
* One limitation on windows - use the same drive for all objects.
* At the conference we were at, there is something called rez, object packaging system, that theyre pushing.
