# TSC Meeting - 1/21/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb [APMG]
* Guthrie [Amazon]
* Jan Hanca [Robotec.Ai]
* JT [SCB_GameDesign]
* lsemp3d
* Naomi Washington
* Nick_L
* null  [meta]
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Tobias Alexander Franke [Huwei]


## Meeting Notes

### Announcement - Naomi Washington [LF]
* Reminder - Joe taking a back from Sig-Release chair to be director of O3DF full time.
* No takers so far, for Sig-Release.  Whoever wants to be chair, we really need one for that.
* Reminding the community.
* I saw a note in a channel, a community member had some questions and wanted changes for the website landing page.
* I will connect with that person to see whats on their mind to see what we can do.  we did the revamp 2 years ago, it was
  Well on the way, hopefully we can start a doc and figure out what we can change and cannot change.

### Discussion - Jan Hanca [Robotec.ai]
* Google summer of code contributions have started.  Should GSOC be something that O3DE works in?
* Naomi:  we don't currently - we don't know of any members involved.
* Naomi:  We will pull the number of events we participate in it.
* Jan Hanca:  Its about getting money FROM google to participate as an internship. We'd have to write a topic with the idea,
  and then if accepted they will grant funding.
* JT: there is some travel involved for mentoring and training, but google pays for that.  There is no expense by the organiztions.
* JT: Used to be only university students to participate.  all of that has been historically paid by google.  they have been changing
  details every year.
* Jan Hanca - my experince is 2005, it was the time I participated in the program as a student.  For students only, paid by google, 
  I applied for it as regular internship.  GCC compiler.   The only thing I got from GCC to help me through to give tasks and help through
  and check progress.  From the student's point of view.  If we wanted to do something liek that for the o3df we could get someone to work
  for us for summer?
* Naomi: Please CC Joe and Me about this, start this conversation.  

### Discussion - Jan Hanca [Robotec.ai]
* Next saturday there is an event in brussels (Belgium EU) about open source.  My talk about O3DE was accepted, and will be giving a brief
  explanation of what O3DE is and why its great.  
* I wanted to raise an issue about tests.  This is something I mentioned about tests, right now extras repo we are locked for 2 weeks.
  We were not able to run any successful ar run, so I don't have any problems waiting for solutions from Mike, but I wanted to mention it
  because we have some small fixes we would like to get into the point release, and we are not currently able to put a single PR through the
  pipeline.
* Sid_Moudgil, There is an issue that galib has uncovered and has put a fix in (PR).  Deadlock introduced by another PR, and he's addressed that deadlock.  AR is currently failing.  I'll take a pass at it first thing after the meetings this morning and we can get merge in.
* Sid_Moudgil [Amzn] - technically o3de extras could contain core functionality.
* Perhaps if we did a Last Known Good AR pull?
* AR - do we have any mechanism and invalidate the cache?

Actual issues
* Dev went red for a week - nobody noticed
* AR was green, but dev was red due to caching issues
   * Script canvas fingerprint didn't take into account that the cache needed rebuild.
* Extras went red because dev was red but not through anything fixable ot checked into extras
   * establish a last known good dev build target that?
   * use head dev, only run the tests that are in o3de-extras?
