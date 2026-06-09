# TSC Meeting - 6/2/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Hellaenergy (Nick) [Red Hat]
* Hex
* JTc[SCB_GameDesign]
* Matteo [Loherangrin]
* Mike_C [Amazon]
* Nick_L
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

### Announcement - Hellaenergy (Nick) - 26.05 was officially released.
* It went well, a couple hiccups, release notes syntax errors, spelling errors, and there was
  a user reported multiplayer template issue which we had to fix quick.
* We have been getting positive feedback.
* JT: We are working on promotional blurb for linkedIn.  We want to make sure we get a shot at it.
  With every release, I do monitoring of socials, and websites myself.  I track numbers, and find out what hits,
  what news wire wins, and since we haven't done OUR release, we haven't gotten much traction.
* Phoronix has published, and grabbed it right away
* A Few of the AI websites have repeated it, but they are insignificant.
* We haven't gotten search engine traction, if you search for "o3DE" on news, etc.
* This round, we hope to get traction for the release.  Obviously we decided to wait, and make sure everything
  smoke tested.  Now I'm pretty confident.  We'll pull the trigger on that, get it out on linkedIn and get it
  posted on other places, follow up on that.
* We had a community outreach meeting, and in the channel we have the summary and notes.
* Mike_C: We'll go see changes in our download numbers, we'll see that later this week.
* JTc: I do a 12 hour, 24hr, 3 day, certain markers to see how things grow.
* Hellaenergy: Do we maintain that reddit channel?
* JTc: We have a reddit, subreddit, and a lounge.  Gaian and I are the 2 most active ones.  I'll take over
  moderation of that as part of the moderator team, and help anyone who wants to take over the channels.
* Not everyone engages via discord - we have to engage github, and reddit.  It spreads faster.  Many orgs
  track what happens on reddit. I'll be opening it up and mentioning what I know next week so we can hit
  a very good reddit moment.  Days separated is preferred so that I can see a different bump in the numbers.

### Announcement - Mike_C - Demo games (MPS)
* Mike_C: Quick note - I'm starting a little work on MPS build on whatever the latest main version we are
  using going forward.  There are some finagling to build and re-sign it, hasn't been done since 24.x, 
  last been posted on o3de-binaries.  Sounds like we're converging on having that available for use as a
  showcase of sorts.  That work is starting initialy on jenkins, then moving to Github Actions builder once
  I figure out how much resources to build it.  It shouldn't use much - use the prepackaged installer, 
  running project build for MPS.  If we have to make some decisions aobut it, we can do that once I get
  it out.
* JT: We can try getting all the others - planet survival, newspaper game, we need to get artists in.
* Mike_C: I'll let you know JT what's done and URL to test it out.
* Mike_C: Working with linux foundation IT to get off of AWS entirely.  If there is a problem, I'll bring it
  up.
* Mike_C:  If FBX file was first defined as text, then binary, in MPS, etc, then there will be a LFS bloat/git
  bloat.
* Matteo: LFS - I think that if we can cut the costs storage, for example, we have atom-content-gem that is
  providing sponza, other materials, I think that we can move it to other repos, for these demos, not in th
  code one, we can cut about 800mb from the LFS.
* JTc[SCB_GameDesign] - I've been mapping out resources that users get, and nick brings it up once in a while
  and there's no concerted effort.  I'm going to be moving a lot of stuff to github, and maybe that can be
  permutated into this.
* Long standing ticket to reduce assets.  Probably needs a review/lead.

### Announcement - STARS
* 9300 stars on GITHUB

### Discussion - Steve P - QT6
* Question about Qt6 merge to development.
* Basic Test Done
* Mac ARM64 update too
* I would like to see reviews and testing on platform, sig-content.
* https://github.com/o3de/o3de/pull/19567
* Nick:  Any show stoppers?
* Steve P [Amazon] - None we are aware of

### Discussion - JT - Asset Processor work
* Community, looking at asset processor community into sig-content.
