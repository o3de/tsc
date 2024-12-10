# TSC Meeting - 12/10/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb [APMG]
* guthrie [Amazon]
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* lsemp3d
* Nick_l
* null [meta]
* Reece H. [DrogonMar]
* Roddie Kieley [Red Hat]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - none

### Discussion - Joe
* December - applying to get a grant from Cesium for a grant.  $50k maybe?
* Will talk to Sig-Graphics - its a huge part of the implementation.   If they give us the grant, we won't be starting from scratch.  There is an implementation it will be updated.  It would be a contracted, limited timeline.  There'd only be enough money for 3-4 months, which should be enough time, I will reach out to everyone involved.  I will reach out to Sid for graphics/audio, which might be Akio.  We can find out.
* Sid: They have their own tile based stream system, and it would pull tiles up, and it would pull in the correct LOD, it should work as-is.
* Sid: The only thing I can think of to make that beter is true streaming.  Would be like META, would be true streaming geometry from disk.  That sort of system which cesium would be kind of doing would be more on the atom side.  There is nothing new I'm aware of it should just work.  I would need to better understand what the need is here.
* Sid: If you need a new feature which does not exist, you'll need more people, investigation, RFC, etc.
* Nick: https://github.com/CesiumGS/cesium-o3de
* Nick: https://cesium.com/

* Joe:  We also have a Security Grant coming, fairly sizeable, could be used for CI/CD pipeline, or finding and resolving security issues in the project / creating plans and tools for responding/recoving from security issues.  I'm being generic on the amounts for now.
* Joe:  At that point what we would do is contract a couple of people (3-4 ?) to help Mike with our CI/CD pipeline and then making sure we resolved all the security issues that we can inside of O3DE itself.  
* Joe:  In particular, government entities require you to get a certification before they will use your software.  Part of that is around security.

* Joe: A  company using 24.09.1, they are bringing up a few issues
* Joe: Performance and Stability -t hey have a lot of crashes, we haven't had any more information in that discussion.  I will we will forward infomration to the sigs as we get it.
* JOe:  They've added quite a bit of functionality to O3DE itself.

