# TSC Meeting - 6/16/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Astin(Chogan)
* ChristianHinkle
* colinb[apmg]
* Gaian [Genome Studios]
* JT [SCB_GameDesign]
* Mike_C [Amazon]
* Luis
* MIke_C [Amazon]
* Nick_L
* Steve P [Amazon]
* Shauna [Genome Studios]

### Announcement - QT6
* Qt6 is live in development!
* AzQtComponentsPython
* Qt For Python - It needs an Application, C++ launcher for python.
* It needs a Qt Application, and you need the style sheets and everything.
* Once that launches, once the singleton is available.
* Gaian: should we consolidate the fixes for styles with the theme system?
* JT: If people can start making notes/written notes I'd like to put together a blog post
  on this Qt6.  Shauna and Reece and I in the last outreach meeting used the blog post to work up to the release,
  we should have more engagement AFTER the release happens, not just before. 
* I'd like to collect information as some of us worked with Naomi as we work for the community to take over responsibilities.
* We have to keep in mind there is a lot of stakeholders - there are people using our editor, they might want to keep using
  this tooling for their workflows.  There are people who just use Atom, for example.  Its because they have customn tooling
  in Qt already and don't want to rewrite it.  At least one bigger blog post and a couple more would be good before the fall
  release.
* colinb: Which version are we on?
* nickL: 6.10.2
* nickL: 6.10 is supported until october this year.  6.11 next year march. 
* nickL: there is no LTS that we can use, we are waiting for it.  6.8 was the prior LTS and isn't suitable due to lack of wayland
  components.
* Steve P: The merge now supports (unoficially) mac silicon, we didn't port qt5 to mac silicon but we did qt6
* Minimum MacOS is 13 (ventura).  You need to get a metal plugin for xcode.
* Steve to get build steps / reqs available.

### Announcement - JT - For outreach 
* I've been keeping an eye on the subreddit, its getting more activity, people are responding sooner, etc.
* I wanna keep developing that, and the moderator team is extended.  I'd give you updates there.  If you're
  predisposed there to use reddit, then take a look and pop in.  Joe / Naomi have the admin keys.
* I plan on leveraging it and using it however we want to use it for the community.
* Gaian - Moderation team on that channl/server is incredibly archaic.  We need get people able to perform
  moderation on that.
* JT: I'll take the lead.

### Discussion - JT
* I want to activate our twitch and mastodon channel (LF).
* I want to move it onto a more community centered channel.
* If you're into twitch, you are in that, then let's start thinking about putting things out on twitch, etc.
* Moving a lot of my work (JT) strictly to this fall release, to github.  so people can see it openly and engage.
* I'll work with you steve on getting the mac stuff updated on github.

### Mike_C - MultiplayerSample
* MultiplayerSample built on 2605 with the new version.
* I put a link out on testing.  I also got the debian version built, and haven't got a chance to test it.
* That pattern will likely be used for other projects.  
* I'll put the link out again, in the content channel for people to try.
* I don't know if we have a release schedule for those.  If its okay, we just replace it in o3debinaries.
* I did run into issues for some order of operation for bundling the assets, and Ir esolved it, but for the most
  part, multiplayersample boots the game, starts the server, you can connect to it locally, don't have a regime
  around testing it.
* In terms of getting it in GHA, I have the bulk of it there, except for the signing.  I don't want to expose the
  deployments to the public for that particular part.
* Working with Nick on formal where they can start attaching particle effects and sound files.
* Actual SIG-network is where MPS belongs, we can link and forward.

### Nick_L - Entity Driven Startup - Heirarchial activation
* https://discord.com/channels/805939474655346758/1426268617124614175
* There isn't necessarily a right answer here.
* Gaian [Genome Studios]
* JT - Everything relies on transforms and so on, and states.  So this is critical.
* JT - We should be able to bring in other developers.
* JT - I want to make sure Gaian has plenty of time to talk to people on voice on this.
