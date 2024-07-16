# TSC Meeting - 07/16/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Guthrie [Amazon]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* Luis Sempé
* Mike Chang [Amazon]
* Mike S. [Carbonated]
* Naomi Washington
* Nick_L 
* null [meta]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Agenda items

Agenda Topic: https://github.com/o3de/tsc/issues/132
(No topics)

### Agenda Item (Ad Hoc) - Maintainer Cleanup - Naomi Washington
* If your maintainer has not been active for months, please delete them from the teams.
* Nick / Naomi / Joe to do the final steps
* We intend to do something similar to a "bug bash" but not a bug bash, to download and test.  QA basically.
* Colin - if we can't contact the chairs, what is the routine?
* SIG-Chairs know the people so its best if they do it.  If you know a person is not active, feel free to go do that.  I'm happy to reinstate if they have gone inactive for 6 mo.  We can always reinstate.
* Sid_Moudgil : Chairs have the ability to remove from the maintainer.  If you are a maintainer you have the rights to remove people.
* Naomi:  Mascot challenge is still open, closes on friday.
* Naomi:  Next step is creative services dept, comb for viability.

### Agenda Item (ad Hoc) - release RoddieKieley [Red Hat]
* There are a couple of dates for cutoff, but nothing unexpected happening right now.
* SIG-Release met with SIG-Docs etc, to get the docs repo to work better with branch synchro before we get too close to the release so we can make sure docs in good shape for the release.
* colinb: Branches matching on all canonical repos?  Are we making a release branch for extras?

### Agenda Item (ad hoc) - Jenkins and extras
* (technical discussion to fix the problem )
* https://github.com/o3de/o3de-jenkins-pipeline/blob/62eb8cede8a34ddaa470a64240051af93eeba872/jobdsl/o3de_extras.groovy#L69 will need to change
* Short term: we will expose on the gui
* Mid-term: we will make branch matching function
* Long-tem : to discuss.
* AR Priorities:  Reliability first.  Then making it easy on users to use.   Then making it fast / cost reduction.  Neck in neck, but reliableness is first.
* Reliability impacts all the others.
* Joe:  Its okay to disable a test and look at it, instead of making people wait and spend extra AR cost.
* If there is a test that is problematic and is not a legitimate test, disable it!

### Agenda Item (ad hoc) - Joe
* I'll be at siggraph
* In august I'll be in hong-kong for the open source summit 
* I'll post an event date somewhere.

