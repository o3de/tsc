# TSC Meeting - 6/24/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L.A.
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* JT [SCB_GameDesign]
* Matteo [Loherangrin]
* Mike S. [Carbonated]
* Nick_L
* null
* Reece H. [DrogonMar]

## Meeting Notes

### Announcement - JT
* MPS Repos I been working on
* Getting them memorized, familiar with them, refreshed and refurbished MPS repos for october release.
* On the other front we're getting everyone coordinated for the mac build, currently looking at piecing
  together qt5 or qt6 discussion ongoing.  Hopefull we'll have mac building by the next release, possibly
  fully supported by the next next release.
* colinb: MPS maybe we can get one working repo that everyone can work on and put together.
* JT: it needs a lot of love.
* There was a reason they split it into two but I digress on that.
* null: due to wanting people to be able to reuse
* JT: licencing issues.  Some assets are CCO but some are mixamo and such
* Nick: We kind of need a reusable free license character (that can jump and shoot and so on for starter asset)
* null: The script canvas hooks came later, the base character controller is all c++
* null: The last few features in there, Darrin was our pseudo-designer and had all these cool gimicky mechanics
  and we sourced the assets for them, and we did them all in script canvas.  Teleporter and jump pads are all
  locally predictive, reconciled later.
* JT: I was hanging out a lot in networking and Ir emember a lot of it popping up.  ITs well worth the time
  for me, and do the outreach in my groups, so I don't have to engage fully with the engine, just the MPS
  and assets.  BUilding up community.  Feed into the main group here too.
* Looking forward to it, it will be quite beneficial to the community.
* Same thing for the particle system, hacking it a cheapo simple one, using free one.
* Colinb: Licensing of the engine (we are available as apache2 + MIT)
* Colinb: Might be best to have their own licencing information for each object.
* JT: Some companies might balk if theres a bunch of mixed licenses, and it is something that needs to get some
  love as we cleanup.
* colinb: I'm making some changes in the schema 2.0 stuff, the object file does reflect the licencing file information
  and so that I can make any changes necessary.
* colinb: also working on schema2.0 licensing, when you compose your project and build it, it will automatically scour
  all the objects you're using and extract the licensing information and put it in a master file at the root of the
  project.
* JT: This is a whole movement in open source, license auditing.  AS the engine grows a lot of people will respect that.

### Discussion - Matteo (Lohaerangrin)
* Regarding releases - we are starting the next point release version.
* At the moment there are no blocking bugs that we need to address quickly, there are additional fixes that did not
  go in the major release and will be nice to have before the october release.  Nick has flagged most of them with
  a dedicated label.
* Every sig is invited to contribute their needs.
* Target date not yet decided for .1 release.

### Discussion - JT 
* We're getting a lot of people that are new, and we want to encourage them
* Some of the new people are general community members, we call them enthusiasts.
* Also mid studio PRs and big studios PR and feature requests coming in.
* How to do a PR?  There are still some misunderstanding by the community in general.
* Also, the volume of PRs are getting more respective about the importance of the PR.
* So one to make sure I'm looking at the docs, I have some adjustments for the docs at the foundation level, on
  how to do a RFC.  
* action item, fixing the docs, what to modify in an RFC.
* Nick: IUs there a "how to get started as a  contributor?" or do standard github guides work?
* JT: Its standard enough compared for normal github for standard guides to work.
* JT: I want to make sure thats not excessive noise that will clog up channels.
* Colinb: I'll share an experience, I'll try to contribute to the docs, I found it very very difficult
  Its looking a lot better than it ever has in the past.  Still has a ways to go.  I'm concenred about how hard
  it is to contribute to the docs.  Specifically the website.  
* Colinb: I went to the "contributing to documentation procesS" on the website, setting up hugo and there's
  dart-sass and NPM and go lang, and our system seems to be fairly fragile, it requires exact versions (older versions)
  of these pieces of software that aren't documented somehwere and it took a long time, I gave up on windows
  and moved to linux.  I'll retry on windows today and get it working on windows today.

### Discussion JT
* HDR is getting prevalent again


