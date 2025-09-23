# TSC Meeting - 9/23/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L.A.
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* jayrulez
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Lohangrin]
* Naomi Washington [LF]
* Nick_L
* null
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Matteo [Loherhangrin]
* We are creating the release notes for the october release.
* We need more detailed descriptions of the most important feature we want to highlight.
* If you have free time in the next few days, look at the draft of the release notes and submit suggestions.
* Jan - Status of release?  Are there any open issues that are still being worked on, are we going to be on time?
* Matteo - No major bug that is open, but I think that we current lack testing.  We can address in the next days
  because we are going to schedule testing period for the community to help us find bugs and other errors since we
  already reached a good state.
* Joe: We still have installation problems.  Opens project mangaer, gives them no error.
* Joe: We've gotten rid of a lot of the issues, but this particule one, its out of our control - firewalls, blocks
  specific ports, makes it difficult to download things reliably, etc.  That's been our number one issue.  Or if they
  install python and it gets put in a weird spot or whatever, or if they have a weird version of windows, etc.
* Joe:  We should take a look at for a point release.  Might be a good time to do some deep investigation as to whats
  going on here.  
* Joe:  Number 1 fix point release - do not delete after you fail install.  we can't post mortem the issue because
  it removes all the tracks.
* Colinb: Maybe we could have a mirror of the zip files.
* https://documentation.help/WiX-3.10.1/get_a_log.html
* Joe:  Long term, I think your idea of only doing the project manager and having it handle the installation of missing
  requirments for building a project is smart as well, it separates out the issues, makes it easier to find problems,
  resolve. them, etc.  That can be target for release, but we should do zip file and "don't roll back" for point release.
* Joe:  outside a point release, we can create the zip file.  Outside the realm of the installer.
* Nick: we should also publish our fingerprints of our zips.  The installer checks hashes, but zips don't.
* Matteo [Loharangrin] - The problem with the zip file, the problem was not related to the licensing it was python dep
  licencing.
* Joe:  We need to build a BOM.  (Bill of Materials) for all we use or licensing.
* Mateo: Can we move a dep to their gem.

### Action items from above

* Nick:  We need to make sure that cmake thats included is > 3.24 in installer
* Nick:  See if there is a way to turn off auto cleanup/delete in WIX
* See if there's a way to make a clean zip
* See if there's a way to rev the stabilization installers so they don't hash collide.

### Discussion - AR Failures
* This one was caused by bad asset builder - and we don't do any asset rebuilds during AR.
* Joe: If we can move to GHA actions after 25.10 - that would be ideal - make sure release is solid, switch over.

### Discussion - Joe
* Joe owns our discord server
* Promoted Gaian to an Admin - they've handled a lot of discord work, reorg, etc.  Gaian is an admin

### Discussion - Colinb versioning
* Versioning RFC - https://github.com/o3de/sig-release/pull/354
* Added something on the bottom about LTS.

### Discussion - Current State of Particle System
* can we figure out a proper brand or consistent name?
* Maybe a contest?
* Not "Particle McParticleFace"

