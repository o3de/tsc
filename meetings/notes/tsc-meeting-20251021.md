# TSC Meeting - 10/21/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* jayrulez
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Nick_L
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Steve P [Amazon]

## Meeting Notes

### Announcement - JT [SCB_GameDesign]
* O3DE now has its own usergroup - ODIE - nov 20th, 9 people coming, in Pasedena CA.
* So cal, open 3d engine users.  THis is a model we used to develop the blender usergroup ecosystem
* Somewhat of a network now, in blender, so for example, we bring in smaller usergroups and incubate those.
* Lets us share the model with a usergroup worldwide.  We'll be posting regular updates, people can copy us, work with us.
* Launched on Thursday.  I've had this in the works for a while, having people side by side helps a lot.  
* Sometimes you just need to have someone right there next to you, thats the superpower of a local user group.
* I'll get people information on how to connect, November 20.

### Discussion - DPKG install
* DEB depends on cmake >= 3.24 
* https://discord.com/channels/805939474655346758/1429926874250739795

### Discussion - Versioning Document
* https://github.com/o3de/sig-release/pull/354
* Hellaenergy - Understanding the history behind it would be helpful.  If anyone knows the historical reason of how we got here,
  it would be interesting.  I've never seen the software backend side be so unrelated to the version of the product before, myself.
* Colinb:  developing a piece of software like this, which is modular, with pieces able to be different versions, with outside
  systems by contributors.  You have to rely on versioning - to do otherwise is to invite disaster.
* Colinb:  outside pieces are starting to be made, and the versioning system is not on its feet yet.  This is the reason
  we are trying to push the versioning stuff now, so that we can get a handle on things, develop best practices, see what works
  and doesn't work.
* Colinb:  O3DE's versioning system is a dotted version number in any of the objects in the engine.  The only one thats really
  had attention paid to it is the one in the engine.json.  The engine can have children objects, like gems, templates, etc, 
  and those could technically get away with not having a version, technically because they're part of the engine and not have
  a versionnumber.  This would work up until we had outside stuff.  I don't think we can do that anymore, I think we really need
  to bite the bullet and treat all the children objects, parent child relations between objects in o3de are nothing more than
  convenience.  You can think of each of those objects as a separate project.  If you do think of it that way you need to be
  able to relate those objects to each other, via versioning, ie, one object can say, "I depend on this object within this
  version, or greater than this version" or something like this.  We need a way to express that, and there are examples
  we've seen out there.  We're circling around python-like semantics to express those relationships, so for example if an engine
  requires gemA, we would say in the json in the engine, we would have a list in there, gem_names, I'd propose something 
  a bit more clear, it would have the name of the gem in the list, it would mean that the gem would have to be any version 
  present. 
  In python you would say I depend on gemA, with some sort of semantic like "> 2.1.0" for whatever the version is.   If its just
  a single number, version 1, version 2... if you have major minor patch, we have standard semver.
* Kind of a concept that snuck into a few places, referred to as engine gems. So when you get 2 installation of the engine on your
  system, that's how it resolves.

### Discussion - Open Particle System
* We still need a better name for this for PR.
* Awaiting public API PR in the works
* Awaiting Android support.



