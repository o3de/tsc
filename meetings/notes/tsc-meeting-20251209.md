# TSC Meeting - 12/09/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]


## Attendees (By Discord name)
* colinb[Apmg]
* Hellaenergy (Nick) [ REd hat]
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* Naomi Washington [LF]
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P. [Amazon]

## Meeting Notes

### Announcement - Hellaenergy (Nick) [Red Hat]
* point release today!  9:30am.

### Announcement - JT [SCB_GameDesign]
* I was at a conference, and had a section about O3DE engine. I talked to about 30-60 developers.
* I encouraged them to sign on and take a look at the engine, I'll give a more detailed report and get a picture of the
  table.  It went really well, had 250 people come by the table, 650 attended total.  8 unity developers, encouraged them
  to take a look at the engine, I have a full inbox to follow up on.

### Announcement - Things will slow down
* Heading towards end of year, after point release, we can expect things to slow down.

### Discussion - Jan Hanca - O3DE Extras will have a PR to pull changes to 25.05 backports
* Branch is not protected, but its a backport of some new features from 25.10 back to 25.04
* Get backport branch, or you can pull those gems with your o3de executable project manager.  we do a full release
  so those releases are included in the repo.json in o3de.canonical.org

### Discussion - AR Github Actions / Mac
* Its getting close, GHA is greener than Jenkins now
* Apple Mac compile is importent but nobody checks.  we sould get it working on GHA
* There is aso ARM support that needs to add, (as in, apple silicon M-chip is just ARM under the hood)
* Steve P [Amazon] 80% of the 3ps built.  Since you can't get older versions of xcode, a lot of the libraries
  needed to be updated, or it would have been too much work.  When Qt6 effort, that got somewhere, there was
  one build error I was stuck on and haven't revisited since.
* Github actions are committed as yaml files in the .github folder in the repo.

### Migrate from custom LFS -> GHA LFS
* Joe:  can you sent me the costs are, for AR, what the costs ar for LFS, and binary downloads, and then
  a written plan is to transfer us over to GH LFS.  that way people like nick, sig release, can review
  that plan, and see if there are any holes.

* Todo list for Infra (Mike C) We need a more elegant way to use a more public tooling to create a BOM.
* Bill Of Materials (list of copyrights, etc)
  Doing security scans, c++ scans, etc,
* Joe: Major Pain Point coming up in a few years to do with EU stuff about security.  We should address
  those as soon as we can.  We aren't necessarily on th ehook for issues, but people who use it might
  be on the hook in those regulations.  We have about a 2 year runway before they go into full effect
  but we have to do right by our users.  I'll go over what we can do in the next 2 years to become
  compliant with the  new rules.


