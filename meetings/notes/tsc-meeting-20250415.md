# TSC Meeting - 4/15/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L.A
* Bartlomiej Styczen
* John Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* lsemp3d
* Matteo [Loherangrin]
* Mike S. [Carbonated]
* Nick_l
* null [meta]
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Matteo [Loherangrin] 
* First code freeze tomorrow - bugs and exceptions major or lower will need an exception
* Getting an exception: Sending an issue in the exception board, sig-release can eval.
* Readme of the exception board has the FAQ. https://github.com/orgs/o3de/projects/69
* Robotec.AI has a standing exception approval for their messaging system that they're doing.
* Joe:  Please tag your issues w/ severity.
* Nick:  Is there a benchmark for what severity is?
* Joe:  Yes, I'll share a document.

### Announcement - Joe Bryant [O3DF]
* Jan to march: 21000 downloads.  Huge increase compared to 10k last year.
* We've been trying to figure out the increase, we saw a gigantic spike in china, outclassing everyone
  by orders of magnitude.
* We found out that Unity was pulled from china and cannot be downloaded from china. Only some 3rd Party version
  is available.
* That announcement came at about the time we saw the spikes in china for downloads.
* We still have to adhere to securty rules, rules around how we interact with people from different countries.
* Anyone can download it from anywhere.  You can see this in the download stats that we have.
* I heard from Cesium and they asked about downloads, etc.  We have users from all over the world, not just
  one or two areas.  We have concentrations - China, USA, Germany, but we have over 100 countries where we have
  downloads.  Some or the more esoteric smaller countries will get 10 downloads, but most of them will have at least
  100.
* null: Whats the status on the localization features that huawei was working on?
* Joe:  We don't want those checked in  becuase they are hardcoded.  What we want to do instead is do the correct localization implementation, making it so that its really easy for people to add languages and use localization propertly, and we can use the version huawei created.  Localization is something we should work on.
* Joe: Central file or series of files that are here all the translations for french or japanese or etc.

### Discussion - Shauna - Call for docs
* We haven't got much in the way of documentation PRs.  If you've made any kind of changes that affect
  behavior or feature additions, please make a documentation PR.  
* Even a little bit of docs is better than none at all
* Sig chairs, co-chairs, please post a call for docs ASAP in your sig channels, as well.

### Discussion - JT [SCB_GameDesgin]
* San Gabriel Valley UX group has had its first big meeting last week (Did not meet since pandemic)
* Talked to 10 of them about o3de. Looking forward to a community base of UX people to interface with the platform.
* I tried to do it during the pandemic, but now that everyones back to gether they're excited about collaborating together
  for projects, and about 10 of them are interested in being contributing members.

### Discussion - Jan Hanca [Robotec.AI]
* Versioning of O3DE - last time during from the release, the 4.2 from dev branch was changed to 2.3
* Are we doing that again?
* Joe - Will discuss this with Mike chang and Nick.  We may have to do a major version increment.  Need nick, Luis, mike,
  to weigh in on that.  The reason for this is that every feature can look at the version and depending on the version,
  they can do things like if you're upgrading for 24.09 to 25.05 and can write code to detect that and choose to do a
  code conversion of data.  I'll want to talk to them about it.  We need to create an issue to update the version in stab.
* Need to talk about stabilizing HOW we do versioning, but those conversations have not resolved.  I don't have a clear
  answer for you right this second.

### DIscussion - Release times
* Normal release time, 
* Its late from europe, we will have to attend the release and will work out the exact timeing for the release call.


