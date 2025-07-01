# TSC Meeting - 7/012025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike S. [Carbonated]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Jan (Impactful change)
* Joe mentions that any maintainers can post in impactful changes.

### Announcement - 4th July
* Joe: 4th of july is a special holiday in USA, people may be slow to respond 3rd to 7th

### Discussion - Next release
* discussion on when the cutoff date is for features in the next release, as well as the fact that
  release is very soon after the prior release.  (Prior one on month ten, this one onmonth 5, next on 10, its not
  balanced).
* Joe:  2 months before release is not enough time to stabilize release.  So we should cut now.
* Sid: There are 2 material parts (2/3) that don't make sense without all of them in.  I'll let them know
  we need to get them in!  
* Joe: For sig-release, its slated for late september or early october.  We want to have enough time AFTER release,
  for a point release, in case there are critical issues that we can patch for roscon.
* Jan: The issue is that we don't have enough time to work on the next release.  We were working to test everything
  On 25.05 (or trying to migrate our clients to it).  With that freeze, its a shortened time, it was something that
  was mentioned, we split the releases into 4 and 8 months.
* Joe:  we're moving back to 2 releases a year.  We got tons of complaints about 1 release a year, so we're going
  back to 2 releases per year.  Each release isn't as impactful as before.  But its easier to stabilize the release
  because there's less stuff in the release.
* Joe:  we don't necessarily freeze the instant we cut the branch.  Freeze is time based, not branch based.  It
  has everything to do with about how soon the feature goes in before the release.  We don't ahve enough time to test
  it if its less than 30 days.  Stability is the most important thing for the engine.
* Ultimately its up to Hellaenergy and Matteo, I'm the Executive Director so its more about guiding, but I don't want
  to lose the momentum.
* We should probably talk about in a TSC meeting, whats the appropriate way of doing changes that will break a 
  lot of users?
* If you look at unity, its maintenence releases, but 1x a year for major releases.
* Unreal is a bit better than that.  Godot is 3mo.
* Jan, we are the only ones implementing anything in extras, if we create a stabilization branch 2 weeks after the
  release, we don't have any time to put anything new in o3de.
* Jan, we should perhaps try to split the release into halves.
* Joe: March/September would be nicer, that would help us better with GDC and ROSCON.  
* Nick: Extras is like an addon repo, the ideal situation for addon repos is that the main core repo locks at some 
  point BEFORE release, and then the other plugin repos have a solid target thats not moving to aim for, that they
  can build and test again, before release.   So it infers that extras repos should not lock on the day that the
  core repo locks, but some time after once the core repo locks.
* Joe: Let us know when we would like to cut o3de-extras.  We have to make sure that there's enough time to test
  stability.  Our current plan to focus on stability is working.
* Joe: I'm still going to encourage us locking down the main O3DE repos early, so we can cut what goes into the
  release.  theres 3.5m lines of code to stabilize, especially the incoming code from huawei is goign to have 
  unexpected side effects.  Need to figure out how to stabilizae all those changes.
* Jan: We need to catch up with the stabilizationof o3de - so I would say get the stabilization branch of extras
  after o3de's stabilization branch.  I will double check what we need to do for extras, as sig-simulation, and
  I would like to highlight by JT, I believe we need a bit clearer information, a bit more in advance of the 
  dates of releases, stabilization branch creattion.  Its catching more than just us by surprise.  We should 
  make this more clear for everyone.  
* Joe: We need to cut in july, for main o3de repo, if we cut for august, 
  we can only stabilize for 2 months and that hasn't been enough time historically.
* We delayed the last one for a month so we end up with less time.  Its always going to be spring period (
    march to may) and I would love to hit march, and then october for roscon.  Everything should work around
    that if possible.  That hasn't changed much - this one was later becuase of issues found and as well as
    the last release was a bit later too.  SIG-release will have to figure out how to keep the train moving
    on time even if the previous release is cutting into the last release.
* Matteo: When you say you like more days in advance to know when the cutoff would be, how much time are you
  expecting.
* Jan: If we know from experience we need 3 months to stabilize, it would be know, fixed dates, at the beginning
  of the year for example - for example, if we know in advance that July, cutting for October, that would be ok.
* Hellaenergy (Nick) [Red Hat] - it was just to create the branches, not cut off.
* Its to make it easier for us to have a controlled environment for testing.  Its easier to pull out breaking
  changes from a stab branch than to pull one from dev.
* Joe:  Now is the time for sig-chairs to let us know what things you want in the next release, here are
  the main beats we are going to try to hit for october.  Thats another thing that people are asking for.
  I need to edit the roadmap again, its not accurate anymore, the particle editor is taking longer for example,
  I am going to go update the roadmap with what I'm aware of.  SIG-Release will eventually be responsible
  for keeping the roadmap together.  But thank yo ufor bringing this up  Jan, all your concerns make sense.
  We have 2 problems to solve - 1 is communication on stabilization branch creation.  The second is 
  things like o3de-extras need to be separate from main as far as branch creation goes.  This does bring up
  another thing.  O3DE extras is ar/vr/xr, I want to break those apart.  I want robotec.ai to own o3de-extras
  and then control its future.  Then we can have AR/VR/XR controlled by meta and have its future.
  Well have to do that in a way that does not break existing users.
* Jan:  Not a lot of traffic for VR. 

