# TSC Meeting - 2/7/2023

## OPEN DISCUSSION

# Chair and Co-Chair
* nick_l[amazon] 
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L [Amazon]
* Tobias Alexander Franke [Huawei]
* geds-dm [Amazon]
* RoddieKieley [Red Hat]
* kberg [Amazon]
* Danillo [Amazon]
* byrcolin [Amazon]
* JT [SCB_GameDesign]

## Agenda Items
* No official agenda items - office hours! 
https://github.com/o3de/tsc/issues/67

###  Topic:  Tobias:  Huawei will create a project board
* Just like Amazon, Huawei will add a project board and roadmap for planned contribution.
* There are a bunch of contributions lined up!

### Topic:  Tobias:  You can actually assign anyone to a ticket, if they comment on it.
* If someone comments on a ticket, they can then be assigned a ticket, thats all that needs to happen for it to work!

### Topic:  geds-dm: Sig-core is nominating
* Election will happen final week of February
* NickL encourages non-amazon participation, especially from Huawei, Tobias will see if folks are available!

### Topic: Include canonical repos in O3DE release process 
* NickL: just as a technical example here, I did try to use the O3DE-extras as expected (add the URL) and it did not currently function
  * Many things did not go right - the extras repos contain no gem urls, the gem.jsons contain no download URL, and the current repo code
  cannot handle gems in subfolders instead of the root. Many technical Limitations means that if we do want to include the extras in a release
  then they will have to literally be included in the release, ie, inside the release zip setup.exe and so on
* byrcolin:  (Hard to capture the conversation exactly here, but talked about the original design for it being something where the repo.json
  is an advertisement file that indicates where the other objects could be found, and doesn't have to be part of the repo at all, just anywhere 
  you can put it so that it can be downloaded and advertise links.)
* JT : talked about how blender's community addons were a high motivator for getting engaged in the community. 
  One of the determining factors to making it canonical and how its done is to overtly set it up to get it into the canonical.
  It was a high motivator for community engagement and could easily get lost in the conversation.
* geds-dm - If you build an installer based on extras, it would have the binaries. 
* JT:  Discussed at the UX meeting.  Danillo was working on this gem system project manger.  They talked about it this last meeting
  Some of the things we talked about here, they worked thru.
  Talk to Josh in the UX team.  It came out in their research that its a soft spot for the user.
- Danillo - The gems in the core cannot rely on that repo, the user would have to download the gem seperately anwyay.
- Colin - Correct, at minimum it would not need a zip file, it would just need a tag for the release.  Secondarily, a zip file made
  of it could be a binary build.   It could be available by some means for the installer, plus link to that S3 bucket or whatever it is
- Danillo a question would be whether the release would be blocked by canonical not being ready or whether it would leave the non-functioning
  canonicals behind.
- JT - The work I'm doing with the USD module camera, would be come core / canonical.
- Byrcolin: core modules are either essential (used by everyone) or required by the core to function.  likely you should put a ticket to put
  it into the repo.  Or convince the TSC that it goes in the core repo.  The core is small, changes rarely, hardened.  Extras changes rapidy.
  Extras can have items promoted and demoted.
- JT - Just again to reiterate that changes should have a mechanism to prohibit.  If you're going to touch somehting, touch it only once.  Make
  sure you can make the adjustments later on.
- NIck:  I'm imagining a universe
- byrcolin - yes the official repos just have links to the extras repos, the repo link (extras) will be for all installs.
- Theres also another list that lives only in the program manager, that has community links.  It can add it to the repo and you can see all the
  objects in the repo, trust it, and get the content.
- JT - this is something familiar with the studio, and heavily modified on the internal studios.  I don't want to paint anyone in the corner.
  I'm prominent in the blender fork ecosystem for boutique studios.
- byrcolin - I can maybe contribute 
- JT - it tends to encourage code contribution
- Nick: (Explained how the installer process creates pre-built binaries, including pre-built CMAKE files, headers, lib files, dlls, etc, that can be used
without compiling but also allows you to link to source.  For example, you can have a source gem, built against a source engine, or a source gem built against
a installer engine, or a built gem against a source engine, etc.  They are interchangeable transparently.
- Nick: Asks JT:  how do they ensure in blender that all extras/plugins work?
- JT:  The community is volunteer to maintain them and do some quick regression tests, etc.  Currently they're pushing it to the cloud infrastructure
 to maintian more control over it.  They're moving more towards a walled garden version of all this, to keep their management needs down.  Prone to
 relying on the community to do the minion work for the module manager.  there are so many modules that sometimes a second developer jumps in and helps.
 organically helped.  So its that organic building up of the community - so the earlier you start the more the community grows.
- JT:  The thing I advocated for and wasn't implemented was to implement a feed back system.  It would suddenly break, slip thru the cracks of the community
  testing mechanism.  Devs would have to rush to fix the addon, so there are dynamics there that have to be wrangled.  It is an opportunity for community engagement.
- byrcolin: In such a scenario, say I have a plugin for the blender, I work it out and it works in the current version.  Does it get included in the next version 
automatically, even if it fails?  
- JT:  Yes, They rely on the people ad-hoc wise, managing this, and it slips htru the cracks.  But thats why I got involved in soft-fork ecosystem.  People like us
can handle a lot of stuff at the time, we can lend our expertise.  The novices, if they're in charge of hte project, the project can go sideways.  It does really
envigorate the community.
- byrcolin:  We have a versioning system, I think geds-dm might know more.  I think it specifies whether or not the object is compatible with a release.  Current
  release forward / unspecified.  we don't have the resources to build or test everyones things.  Unless the person issuing that gem, says no, its only for release X.
- Nick L:  Can put more metadata on it, such as tested in this version, last known good version, etc.
- JT: that's what we do in blender, it says what version its tested against.  when you come up in the addon manager it shows that info.  It makes it obvious which ones
need community testing or upgrading.  That metadata was put in for that reason, having that clear and in the right places allows us to jump in.
- geds-dm:  its being added now.
(Semi-consensus here that the future vision is, a lightweight core and installer, but with already prepopulated repo urls to the canonical repos but not the bulk
data of those repos.  This would allow the project manager to show the various gems available in taht repos, with UX to indicate that they are downloadable/extra
and autodownload if used).
