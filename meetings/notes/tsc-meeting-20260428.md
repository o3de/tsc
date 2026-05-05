# TSC Meeting - 4/28/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Andre L. A.
* Arbiter
* ChristianHinkle
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* Nhiem
* Nick_L
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]
* xdllq 

### Announcement - JT - Outreach Community Meeting
* We had our first outreach meeting
* Topic was how the community could get involved in outreach
* We give community members something specific to do as they join outreach effort.
* There is a calendar feature in the event calendar in discord - you can set an ICS in google or other calendar.
* We will continue the conversation on how to engage.

### Announcement - SIG_Release - Call for help for the release notes for the next release
* Please help out with the release notes.
* Please send a text.md or small doc and we'll do the fancifying into a single document for now.
* Then we'll work on a "theme" of the release, on the top theme will be, what the message will be for later.
  Highlights an verification of the PRs that went into this release.
* We'll resubmit it to the community for review.

### Announcement - JT - IEEE GameJam
* I posted some images in the events channel.
* A lot of future developers, indicataed a lot of problems with the industry.
* Gave the students pointers on how to be successful in the industry, including in AI.
* Its highly competitive, and it looks good due to the quality of the work the students are putting out.
* There's a chance to get work, they got highly successfull people working in entry level positions, so its hard
  to get a job in the industry.

### Announcement - bumping base compiler version for 26.10
* Mike_C - PR is updating that.  In some cases its less than 14, we can mention using an update-alternatives, 
  we need to install GCC, and update it to the verison thats compatible as well.  One of them installed was
  additional tools to allow new versions of clang.
* Mike_C - Sometimes packages itself, indicate it only supports a certain version.
* https://vfxplatform.com/#reference-platform
* Virtual production importance here too
* Mike_C - Have made a "canary" AR that compiles agains the latest versions of clang/gcc and we can see a problem coming up before
  it impacts us.
* Colinb - Ubuntu 26.04 is out, LTS.
* Mike_C we'll bump up when its available on github actions
* Steve P - JT pointed out we're looking at the VFX guidelines - one was python - EOL october.

### Note - Matteo
* We are experiencing an issue in the latest version on the upcoming version
* A bug related to how to handle offset in UVs.
* Sig-Graphics is doing an investigation.  Any help is welcome.
* Other option we can use if we don't find solution - forcing previous behavior on linux platform.  Essentially solved
  the issues, but is acting like in the past.
* Try to look at dx12 vs vulkan and see if the matrix values different.  When you see the values in the renderdoc capture.
* Start with dx12 matrix math and values in there.
* Matteo - New approach of the pipeline puts bindless rendering, to upload materials not uploading the direct access with
  a constant buffer, using indirection.

### Note - JT - We need to comunity promotion!  The LF is rolling back services for this release
* We'll talk about it more next week



