# TSC Meeting - 6/04/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Adam Dabrowski
* colinb[APMG]
* Joe Bryant [O3DF]
* Lloyd T. [Carbonated]
* Luis Sempé
* Naomi Washington
* Nick_L
* null [meta]
* RoddieKieley [Red Hat]
* Sid_moudgil [Amzn]
* Steve P [Amazon]

## Agenda items
https://github.com/o3de/tsc/issues/127
none

## Agenda Items (Ad-hoc)

### Agenda Item - Joe
* Joe Bryant - release meeting on friday.  
* going to ask people to volunteer to do various parts of the release
* looking at the reverse integration plan, to get people to volunteer.
* I'll be at AWE in long beach june 17-20th, if anyone is planning on attending, let me know to meet up
* AWE is a AR/VR conference, one of the largest in North America.

### Agenda Item - colinb APMG
* Sony has contacted colinb about the license for consoles.  This is proceeding forwards.
* (Colinb intends to be try to host a company which can port to consoles).

### Agenda Item - o3de Connect meetup
* Next week wednesday
* Sid do presentation from GDC. June 12th.

### Agenda Item - Joe Bryant - Linux
* 24.09 release will have support for 24.04 ubuntu
* Drop support for 20.04 - deprecated at that point.
* Steve to put a message on General and sig-platform to notify drop of 20.04.
* Steve: Q on that... we are dropping official support for 20.04.
* 20.04 was too old for clang and cmake but 22.04 and 24.04 all by default have cmake and clang versions that are already compatible.
* Joe:  Snap packages will be deprecated.  It has been a problematic system for us to support.  Probably talk to sig-platform / sig-build and leaning towards gradually dropping support for snap. Will RFC to state opinions.
* Steve: I know of all teh pitfalls, I'll write it up.
* Joe: After write up we'll vote and I'll leave it up to those sigs.
* colinb: containerization and docker vs snap, snap is not much of a container its more of a package?
* steve: snap spawns a sandbox, if you create a new project with snap the project needs to be running under the same snap environment
* colinb: To be a real container, it would have to have a virtual environment it runs.
* Steve P - Can we have an alternative docker build?  I'll add it to the RFC.
* RoddieKieley - you'll run into the same problems in all of them, immutable image etc.
* Joe:  We could talk to canonical.
* Steve: The way we do it eliminates the advantage of snap.

### Agenda Item - Joe
* Recent asset browser changes improve startup time 90%
* their projects have many tends of thousands of project
* they are a stress test for all the systems, like startup, AP, finding bottlnecks in all that
* Major QOL improvement for people

### Agenda Item - Joe
* I have created a project life cycle documents, it is now being edited, I'll ask the TSC to take a look.
* Normally this would be TAC, but we only have one TAC person (sid).
* This defines the process for new projects to be accepted under O3DF (not O3DE). 
* We have a case of this that is currently happening or happening soon, but they want the O3DF to manage this particular project (utility / tool / etc) and its tangentially related to the engine, its not part of the engine itself (so not part of O3DE).  O3DE could be a first customer, but its independent.  Those projects would have maintainers, leadership, etc.  Its a project that falls under the O3DF leadership but has its own internal leadership and proecess and releases and etc.
* Every foundation has its own process for project acceptance, we use the ASWF template but each sub-foundation of the LF needs its own process for this.
* We need this accepted before we can accept any projects into the foundation.  Example, CNCF and ASWF have 30-40 projects under them.
* Naomi:  The O3DF is set up as an umbrella foundation.  O3DE is a project under that foundation.  This lifecycle doc is the process to accept new projects into the foundation as sub-projects siblings with O3DE.
* Joe: There is a company that has come to us that wants to open a bunch of code thats used in gaming and simulation space, but they are not o3de. O3DE could consume those, but they wouldn't be part of o3de.  So they would potentially be hosted/owned under the O3DF as a sibling to O3DE.
* Joe: the doc outlines that process - for example, legal review, checking whether it can be open sourced, checking for interest/contribution, and then third phase is what acceptance means, how its talkeda bout by the foundation, what is expected, what is the leadership chain, all of that.
* Naomi: All projects have their own TSC, and one member that represents at the TAC.  
* Joe: The TAC manages all the seperate projects and see where people could work together and keep awareness of all the things going on across the foundation.  Right now we only have 1 project and is thus only have 1 tsc person.
* colinb: Many of the items in the extra repo could be managed that way?
* Joe:  there is some overhead to managing that.  I'm not pushing hard for that stuff to be pushed out.  There is a use case that is perfrect for the lifecycle and testing it and so we'll start with that.  And hten gradually focus on other things.  Let's focus on one and get used to the structure of multiple projects.

