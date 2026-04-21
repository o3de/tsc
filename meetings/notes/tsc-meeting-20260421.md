# TSC Meeting - 4/21/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Andre L. A
* Atmosaero
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Nick_L
* RoddieKieley [Red Hat]
* Steve P [Amazon]

### Announcement - Matteo (SIG-Release)
* After tomorrow, we will enforce the exception process for all the bugs that are found in the stabilization code.
* The process is simple, if you need to propose a bug fix, for stabilization, just send a message in SIG-Release channel,
  we will evaluate the risk about merging the proposal.
* We need maintainers for the samples, or at least reviewers.
* JT: We could community mob-code, live to everyone?  I'll propose that after this release.  I'll work it on getting mob coding
  computers set up.
* Jan Hanca - O3DE Extras is a bit late - we are waiting for ROS2 - release is going to happen right happen after O3DE release.
  We already implemented a few things that are already in ROS2.  We will be pushing them to the stabilization branch - if we
  push them now, we won't be able to build it.  Hopefully there will be a prerelease next week, with last minute changes to
  o3de-extras.  This is something I mentioned a long time ago.
* All the changes are compatible with older versions of the ROS2.  The code is there from ROS2 community, they release it for
  the previous LTS - and then in may we'll have a new release.
* One More PR with the sync between Dev and O3DE-extras.  Stab cherry-picking.
* Matteo: Is there a final date for ROS2 release?
* Jan Hanca - typically 25th of may.  Not sure if there's a date yet.   we will be a bit quicker than that with our release
  in O3DE.  There are 3 ROS versions supported - Humble (2022) LTS until 2027,   Jazzy, LTS until 2029, and the new version
  will be in may, and we'll be pushing our changes to Humble and Jazzy.

### Announcement - JT
* Today is the submission day for siggraph posters.  We have an outstanding submission that we're putting in on the AWSF side, 
  the collective project that ODIE is in .   We finished late last night, abstract for submission, and I'll be submitting that
  before the 3pm deadline for today.  that could be a Major development for O3DE, having that name in the SIGGraph/ACM library.
* We'll be doing a presentation about open USD and O3DE if we get accepted.
* It not, next year, we'll get accepted given the feedback.  
* Any mention in the ACM / Siggraph library is a real honor and a really big thing that people all over the industry will search
  and O3DE will come up.  It was well worth it, and I'm really proud of the submission.  "Collective-Project-001" mentions O3DE.


