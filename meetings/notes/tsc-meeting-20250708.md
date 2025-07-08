# TSC Meeting - 7/012025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Nick_L
* Reece H. [DrogonMar]
* Steve P [Amazon]

## Meeting Notes

### Announcement - DOwnloads (Joe)
* June was the largest month for downlods this year
* a huge increase in downloads, we're on track to far surprass 2024's download numbers.  We've almost caught up with 2024 and we're only 6 months in.
* Joe:  investigation continues with several companies, we will potentially
  be having an integration for services for o3de.

### Discussion - Agenda Item - Toolset (Compiler) to support officially
* Joe: The problem is that our toolset dependencies have not been updated
  to the latest version, also vs to the latest version.  I discussed this
  a bit with nick.  My issue is that if we fall too far behind compared to latest ubuntu/fedora, and we can see friction points with users.  You can see it with people in discord having issues running, they have to download their clang versions and so on.  
* I'd like to propose with the tSC, we should set a benchmark, for a release, we should build with the tools that come with the LTS versions.
* (Discussion ensues about versioning and visual studio)
* we would like sig-platform to develop a strategy related to this - we should
  have a written down strategy we can explain to people, and then on the software side we need to have a documented known good version and range.
* We might consider doing nightly or weekly runs for list.
* another options is to include it on AR.  we might even have an indication
  that it runs on the latest / minimum version
* Joe: We can indicate that we test against these versions.
* JT: we do have to get into the checkboxes, show the documentation about which versions and how to get it.
* Joe:  we're not going to get every latest version, and we should get input from Hellaenergy, from Red Hat and I think a #1 issue is a communication issues, we need to indicate what we support and how to make sure you can get it.  And then the other is to have an amber indicator.
* Colinb: I'll take an item.
* JT: as the community scales, there will be more builders and people who will find and fix these.
* NIck:  what do we actuallysupport?
* Joe:  Last 2 LTS releases.  
* Nick: That could, depending on the release cycle, indicate a nearly 8 year lag time in tech.
* https://github.com/orgs/o3de/projects/73/views/1
* Joe:  Even a tiny change is risky, let sig releasae know
* Joe:  I think for right now, let's go ahead and message sig-release with the information about the issue, or the PR already, etc, lets us have a meeting today, we can discuss it.  with that, I do think there needs to be a section or board that is a proposal board, they are asking if this can go into a point release, the exception board.  Yes its approved/no its not. 

### Discussion - Agenda Item - meshoptimizer - Nick L
https://github.com/o3de/o3de/pull/18711
https://github.com/zeux/meshoptimizer
* We will have to meet the license requirements for MIT, including disclosure.
  See license scanner!

### Discussion - Jan - Dates
* It would be nice for developers to know the exact date of split of stabilization from development, and point release.  
* Joe:  Attend 9:30am PST release meeting, we will communicate out to the sig-all the dates are once we get those figured out.

### Discussion - colinb
* Do we support the latest msvc toolchain?
* Joe:  Once I have the information about what we support I will try getting that up under requirements.  So that people know, "If I use this, I'm fine."
* We should add this as part of the release checklist, we should capture the
  actual version we tested against and communicate that out by the freeze time.

### Discussion - colinb
* we have 2 different ways to fix this
* unname the param void it, or maybe-unused it.  

### Discussion - webinar
https://zoom.us/webinar/register/WN_k6t5GGBuQdedszdpHi2R8A#/registration