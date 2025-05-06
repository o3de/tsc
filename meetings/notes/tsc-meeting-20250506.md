# TSC Meeting - 5/6/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* flynn
* colinb[APMG]
* Jan Hanca [Robotec.ai]
* JT [SCB_GameDesign]
* Luis
* Matteo [Logerangrin]
* Nick_l
* null [meta]
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Sid_MOudgil [Amzn]
* Steve P. [Amazon]

## Meeting Notes

### Announcement - Release Is Delayed - Matteo [Loherangrin]
* 2025.05 release has been postponed by one week
* There are some bugs on the graphics side that need to be fixed.
* We need more time so as to not release something that will break existing project.
* Sid - It may be necessary to postpone it past memorial day weekend, anything working on the graphics stuff
  have been working on their own stuff.  We may need from Meta, Huawei, to have a look, there have been a lot of
  big changes that have exposed these small issues.  I'd be open to push it another week or so.
* Matteo - I will have to double check.  We talked about it yesterday and it was our position was not to go too far.
  I think that has nobody that will pick that issue.   I think only the author of the contribution can fix or is it
  something someone else can pick up?
* Sid: In theory - one with bloom and one with the mouse - in theory they are shoudn't be hard bugs to solve - they
  are easy to repro, not hangs that are hard to debug - but I have not looked at it at all.  At least on locally, 
  so I haven't looked it.  Its up to anyone to give it a try, so we can take a look.  The bloom one, anyone can repro
  it, find out where the NaNs are coming from, is it the UV coordinteas, where is it coming from, etc. 
* https://discord.com/channels/805939474655346758/1369038409577922640
* Another option, do this release, release a patch in a month, when deadlines are over and we can take more time
  to look at this.  
* Joe:  Not willing to do a patch for the bloom.  Its a very large regression.  We could postpone again, we could
  postpone by 3 weeks.  The reason for that, 2 weeks lands us on the date after memorial day, there aren't many
  people available on that day.  A lot of people take 4 day weekends, etc.  If we're going to go longer, we couldn't
  do the 27th, since that's the day after memorial day.  Tuesday june 3rd would be the date.  It would still be
  2505.0 but we'd release on the 3rd.  That's the latest we should delay if we are going to because we start running
  into 1) I'm going to be out travelling for a large chunk of june, one event is in china.  2) we start running up
  against the planning for the next release in october.  Naomi, if we postpone to june3, what we would have to do is
  reschedule the webinar to the week after.  We have an open3d connect on the 11th, that could be the webinar.
* Joe:  Let's talk to may (marketing director) about that.  She's putting together the webinar.
* Sid: I definitely agree with this plan and will try to get the bloom resolved by then.  
* Sid: I'll ahve a bit more time to look into this next week. 
* Joe:  Bloom is the one thing I will not allow the release to go outwith, its just so ugly and an obvious regression.
  It will affect anyone trying to do anything with o3de.  What I'd like to do now .. jan what do you think of the delay?
* Jan: I do agree with the delay, the bloom affects all of our projects, we always use quad lights and bloom,
  in warehouse environments.
* colin: we should be erring on the side of quality.
* JT:  Thats shoudl be find, availibility is okay.
* Shauna: Fine by me
* Luis: Absolutely
* Matteo: That's fine.
* Naomi: Of course
* Nick: I'l be back home by then and it will give me an opportunity to contribute.
* null: I agree with the plan
* steve: sounds good to me
* Joe: Postponing to june 3 for the release.  We will talk about it to oure marketing director.  Not going to change
  any names or anything of the release, I wiill have to talk to Sid and Anton to make absolutely sure its released,
  we cannot delay any furhter than that.  We ahve to do everything we possibly can to get it resolved before june 3,
  which means putting it in the week before, may 26.
* (Discussion about the mouse cursor thing)
* Sid: For PC it should work to share the capture with PIX.
* JOe: thanks for pushing that quality is more important

### JT - IEEE Games Sig 
* IEEE Game Sig in UCI was outstanding.  One of the best ever.  I have a link here.
* https://gamesigshowcase.org/
* I was a walking billboard, talked to game teams, links to the judges, am in email threads discussing O3DE and 
  game tech in general.  Was very fruitful and looking forward to see what happens.
* The discussion and quality of the games and aesthetics was off the charts.  I've never seen students showcase
  that many student teams produce that quality of work for decades.
* Joe: please let me know a couple weeks away, if not months.  I'll be happy to attend next year, I'll need exact
  dates.  Please let me know if similar things, times and dates, and I will try to work those in our travel
  budget so that I can go to them.  I have lulls I can fill in with things like that.
* JT: It really exploded this year.  Usually its kind of quaint.  This year its WOAH.
* JT: I'll definitely be on it for next year.  If other ones are blooming like this, pun in tended, we need to get
  on it.
* JT: Its hard to impress me with stuff like this but I was impressed.

### Jan Hanca - What is the plan for the version of the engine.
* Joe: We're going to 2.4 for the version.  Mikes not here but it looks like 2.4
* We do need to have someone who is willign to lead the discussion on the versioning scheme.
* I need someone (since I'm travlling a lot) to lead that conversaion forward and create a RFC aroudn the proposal.
* 2409 released early in october.  its based on the original date we planned to release.  Its a huge headache to
  change everything.
* Jan: I was more thinking about the internal version.
* Joe:  Keep our same version scheme - but change it in dev? It moves so fast in dev anyway.
* Joe:  That is a conversaion that I trust with people far smarter than me and closer to the problem.
* Joe:  dev versioning moves forward quadruple the speed of main version - so we need to reconcile that.
* Jan:  This is the issue for me, dev branch is always unstable and you don't need to link the products or gems
  with, that much.
