# TSC Meeting - 6/9/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Nick_L
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

### Announcement - JT - Connect Meeting Is Tomorrow
* 8am PST
* JT to work with Naomi to fix time.

### Discussion - QT6 - Hellaenergy
* QT6 is ready to merge into development.  It looks good on fedora.
* There was worry about cosmetic issue, it works realy well.  Nice and snappy.
* I will note that under "native wayland" it is crashing under current NVIDIA driver.
* After this meeting I'll look into it and see if it still exists.
* When you tear down the editor in xwayland breaks.
* It is ready to merge.  It piggybacks mac silicon support.
* Bindless to work is still required for full metal support, and the way to get it to work is you have to
  do work on binding resources on metal.  You have to use argument buffers a different way.
* Fully optimized IOS version METAL already existed.
* xcode package needed to be downloaded, special metal package specifically.

### Discussion - Asset Processor
* Asset processor uses SQLITE in Write-Ahead-Lock mode (WAL).
* Asset processor needs its dependencies to be described in order to function correctly, most cache
  inconsistencies come about from jobs which have dependencies that they do not disclose to the AP
  and thus it cannot correctly describe its dependency tree to order jobs.
* JT:  We had bots pick up on the "Good First Issue" tags and do them.
* I've been rallying the stakeholders in docs to do some subsqeuent PRs to do them.
* Bot PRS take away opportuities from the community to become a reviewer or maintainer.
* I'll approve those PRs and for typos and things like that.
* We should get more people testing!

