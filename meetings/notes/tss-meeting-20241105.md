# TSC Meeting - 11/05/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb
* Guthrie [Amazon]
* Joe Bryand [O3DF]
* JT [SCB-PasOS]
* lsemp3d
* Mike S. [Carbonated]
* Naomi Washington [LF]
* Nick_l
* Sergio Rojas
* Shauna [genome studios]
* Sid_moudgil [Amazon]
* Steve P [amazon]

## Meeting Notes

### Announcement - Release - Joe
* Joe - tomorrow is the 24.9.1 point release
* Its a bugfix release, no new features and etc along those lines
* The PR for the release notes is up
* We have an offline install download
* We also will have release - 1 available for slower migrators
* We haven't seen a lot of activity due to roscon
* We HAVE seen a large set of activity due to release of the new version.
* We told everyone to downlload the deb package and get a feel for it first and we don't get stats for that.  Mike C is going to give us the download numbers for deb packages today and we can see.
* I'm out friday-sunday this week, will be difficult to reach during that time
* back for a week, then out again, for the LF member conference.  I'll be giving a talk on the state of open source in gaming.
* Then back for a week
* Then out for thanksgiving and headed to a FL, USA conference.  Meeting people and suggesting O3DE
* Colinb: question - directing to the debian package download?  was it updated?
* Joe - yes, its updated, the snap was discontinued.  We offer DEB an RPM
* We'll talk to canonical about snap, it was not a super high priority right now.  A lot of people are having issues with snap packaging due to how it handles dependencies and how it handles isolation.
* Mike S. - 24.09.1 release - in the PR link, does not give me release notes.   
* JOe - link in chat to rich diff https://github.com/o3de/sig-release/pull/299/files?short_path=f13652f#diff-f13652f8f64c4bff122d6e23ca0b0dfbfb9b5cfdd7fb828453f6fbd29b86e03e

### Discussion - Joe
* Many complaints about our versioning system
* The main complaint is diff between `main` and `development`.  Main tracks slower than development.  
* Joe - we should start a conversation around versioning and how we can get better consistency between development and mainline.
* Sig-core makes the most sense.  I don't think it will get solved in a TSC meeting.  A thread opened in sig-core?  Start a small unofficial WG.   
* One requirement to put down is to be compatible with our current versioning.   Cause undue pain, etc.   
* `main` runs at version 2.x.x while dev runs at 4.x.x and when we cut stabilization it means that their stuff cuts bck from v2 to v4, and they have to do emergency fixes and stuff.  
* Joe:  I'll put a small doc for sig core, and what the complaints are.  We need to have a discussion and I don't have a solution.  Sig-core is probably the best to discuss this.
* Joe:  Nick needs to be involved.
* Joe:  If it should be fixed, and how we should fix it.
* Colinb:  A lot of the schema 2.0 stuff is to do with versioning so I'll be there
* Joe:  Keep it simple and easy to maintain.
* Colinb:  Difference between release version and the versions of the pieces of the engine.
* Joe:  Let's separate out the schema 2.0 thing, but I want the problem separate from schema 2.0, so I'd like to keep it simple.  I'll do the problem statement.  Joe can comment / create solution proposals.
* Joe:  once the sig has started honing in we should do a RFC and get community input.

### Discussion - Joe - next release
* We are deciding which dates to do the next release and have to decide between march and may

### Discussion - Colinb - Compliance with exec order 14071
* Enforcement of Russian Sanctions.  Action has been taken on certain Open Source orgs.
* Joe - Linux Foundation does have a stance on this. and remedies.  We have gotten the communiation from LF.
* Joe - we are already compliant.  If there is a maintainer that is associated with a Russian entity, they cannot be a maintainer on the project, it pulls us out of compliance.  Entities, like, companies or government entities, or do business with russia, etc.
* LF is a USA company and thus needs to be in compliance.

### DIscussion - Sid - OBJ Format
* OBJ support works.
* There was no way to test all the formats.
* JT - Obj libraries are in backlot, we fall back to obj, etc.
* https://en.wikipedia.org/wiki/Wavefront_.obj_file
* JT - Ultimate fallback.  Its not the amount of people, its the importance of the group or people, that would cause us to cater to that need.
* colinb - no reason not to have it work
* Sid - going to enable it similar to usd, usd only supports static meshes, but animations need us to update assimp and etc.
* Sid - there's always some unsupported thing, but its not going to be the mature one and you should go to, obj is the gateway format that people have easy access to and get downloads.
* JT - sophisticated workflows due to it being a fallback that always works.
* JT - if they have a specialized use they can go thru it and support it.
* JT - obj sequence - guarintee to get your morphs to work right.  Fake and early point cloud stuff.
* JT - very advanced workflows, hung on to for years and put it into advanced workflows.
* Joe - for anything we decide to turn on, or to utilize, or create a feature, I'm a firm believer in release early and release often.  Turn on OBJ, get that out, and iterate as needed.
* JT - we can always throw together a sample gem for example.
* Sig/content is the best place.
* ASSIMP supports 50 different formats.  Let's not enable all them just because it can work.  Let's not take it as license to turn everything on, its there.
* Joe - pipeline to get blender to o3de?
* Sig/content perhaps?
* Joe - where is the source assets for ODIE?
* Sid - Robotec's point cloud gem works very well

* Joe - release is tomrrow morning 10am, async, and probably about 1/2 an hour
* Joe - I looked at the pRs it all looks good.



