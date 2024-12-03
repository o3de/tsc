# TSC Meeting - 11/19/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Guilaume [Cloud Imperial]
* Guthrie [Amazon]
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* lssemp3d
* Mike S. [Carbonated]
* Naomi Washington [Lf]
* Nick_l
* null [meta]
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sergio Rojas
* shubh
* Sid_Moudgil [Amzn]
* Steve P [amazon]

## Meeting Notes

### Announcement - Joe Bryant [O3DF]
* I have officially put in notification that I will be stepping down as SIG-Release chair January 10th.
* I am happy to mentor whoever takes it over, but I need to focus on the executive director role for O3DE/O3DF.
* I'll be around but not as involved.
* I will work with Naomi on Timing for nominations, and probably have an extended nomination process.  Its a highly visible role and you learn a lot.

### Announcement - Joe Bryant [O3DF]
* we are revamping a lot of the O3DE information for the public, to note all the changes over the year.
* We are focusing less on metaverse and more on game, simulation, film and video, robotics.
* We are going to see things change based on how we talk about O3DE, even though I think metaverse has a future, I don't think its now, and we have very finite resources, so the time we do spend, we spend more on games, etc, less on metaverse.  Everything we do pushes us towards metaverses, but right now, we focus on game, film, video, robotics.

### Discussion - Jan Hanca - Question to Joe
* Jan: Sig-Release question - I saw a message on the text channel about the releases and planning for the next year.
* Jan: Is there anything to share?
* Joe: The board approves having a release in May 2025, and another in October 2025.
* Joe: We are going to aim for may, but if we don't feel the quality is there, we will ship once we feel the quality is there.  2409 proved that we get really good visibility and coverage if we make sure the release is a quality release.
* Jan: Point releases planning?
* Joe: Point releases are ad-hoc and we only release them if there's a need.  Point releases are supposed to fix issues.
* Joe: There's 2 current issues that could be a point release candidate, one with ROS, one with GameLift that was brought up.  The gamelift one, I am concerned about, its not a huge priority, its a 3rd party thing.  We need to gain a better understanding of the ros issue to know how the issue is... some issue with timing and ubuntu versions and releases.
* Nick: why is the Gamelift gem still part of O3DE, it prevents Amzn from updating it as they wish
* Joe: Agreed, we're going to talk to them about updating it or moving it out, so that they can update it at will.
* Joe: Breakage can happen over a long period of time (like cesium) we should not have internal O3DE updates to keep gamelift running.
* Colin: last I talked to mike about it, they said AWS had a server for us to use, I wrote a procedure for how to move the gems out and preserve the history, they would just need to actually get around to doing it.
* Joe: Can I meet with you (sid) and Gene about doing this?
* Joe: We need to separate out gamelift.  Its requiring a lot of engine updates, how can we prevent that.
* Joe:  Its not something that broke in the engine, its a reliance that the gem has with a setting in the engine.
* Sid: FYI it would have to test with the gamelift team itself.  They'd have to find the resources to do this kind of work.
* Sid: whatever the easiest thing, do that, if you're going thru the whole 'lets move stuff out' its a long term thing and you'd need gamelift team support.
* Joe: We might still move it into the .2 or .3 release.  But even if so, long term, we need to move 3rd party gems out of the repo.
* Sid: Yes, its a matter of capacity.
* Sid: We can setup a meeting but I think even with the existing team, I pinged them and asked them if they are able to provide support here.  so I was a little bit worried on the expectations wise.
* Colinb: I'd like to be part of that meeting.  I don't think its going to be too much of a deal.
* Colinb: Brings up an interesting point - if there are very important gems or plugins we could make that part of a monthly build or test, make sure it links or runs or something.
* Joe:  The LF has made it very clear to me (by the leadership) we do not condone one member's features or products or services over another, becuase if you look at our board, we have competitors that are working together to help O3DE become the best it could be.  We have to maintain a neutral stance.  Is AWS important?  Yes, absolutely, without AWS there's no o3DE.  But we cannot give Amazon services more preferences over others, for example, perhaps Microsoft does Azure impl, why is AWS officially part of O3De, while theirs is on a separate server?  
* Joe: I need everyone to be treated the same, for 3rd party products and services.  I had a similar talk with houdini sidefx, we do offer as a member a lot of co-marketing and stuff like that.  Liek in sideFX case, we can tell people here it is, you can grab it.
* Joe:  I don't want to be showing partiality to different companies stuff, that's not a good look.
* colinb: Its not just theoretical, I've heard from large companies saying its 'amazons engine' and has 'amazon stuff in the engine'.
* joe:  that being said, right now we are in conjecture land.  Bringing it back to reality where we are right now.
* sid: We still have to go thru an approval process, whichever repo it goes thru.
* sid: We need a gem discovery system.
* colinb: https://github.com/o3de/o3de/issues/18419 rfc for discovery.

### Announcement - Joe
* CI/CD is moving soon to Github Actions.
* Please report issues!  
* Once we start the transition we expect issues, so report them.
* There has been 6 mo of testing for it.
* We literally cannot continue to afford CI/CD if it keeps growing like it is right now.
* It allows people to duplicate our CI/CD pipeline internally or on their own forks.

### Discussion - Reece H. [DrogonMar] - I'll post the issue
* https://github.com/o3de/o3de/issues/18513
* I'd like to know more about Qt.  As far as I can tell, the Wayland QPA does not support native event filter.
* Every platform the editor touches uses native event filter for input.
* Steve: I have rebuilt the QT package with wayland enabled, I'll talk to you offline about it.
* Steve: I'll send you a message about it, the changes would require another Qt version (wayland version package)
* Steve: They are different build flags to build a wayland Qt vs a XCB qt.  it was an extra additional project outside of Qt.
* Steve: It replaces one of the plugins to disable the XCB.  
* Reece: Maybe its a latest qt thing.
* Reece: O3DE uses an older Qt version.

### Discussion - multiplayer template release issues
* .2 
* Joe: Roddie - sig release - talk about timing on .2 point release.
* Maybe one more thing In serialization of AZ::std::string if its there its another reason to .2
* Prefab overrides, weird crashes.

### Discussion - Nick L script canvas upgrade issues
* lsemp3d sc has a built-in mechanism to upgrade the nodes
* lsemp3d: It has a version converting mechanism of the engine, so the support should be there
* lsemp3d: There also has a tool that can update everything to open/resave/run the conversion system.
* lsemp3d: Just include me, I'm happy to help out.
* lsemp3d: It should notice that node topology has changed and requires a resave and to auto bring the node into the new format.

### Discussion - Joe - upgrading - reminded me
* Guilliarme posted concerns for the graphics sig - a breaking change for the graphics sig was posted, and could not upgrade without
  making a change to the project code.
* https://discord.com/channels/805939474655346758/816043793576886273/1313538079595823194
* But - his concern was, is there a way to automate that. Is there a way to fix it...
* Let's see if we can solve this with automation somehow?
* SIG-graphics-Audio
* Guillaume: To lose all the samples right away because of this change would be a big loss
* Guillaume - Config files that are there to help you customize the render pipeline - but its not a thing you often do in a game jam project.
* Sid_Moudgil - he changed the template, the project can add stuff to the SRGI for your use case.

