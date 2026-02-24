# TSC Meeting - 2/24/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* colinb[APMG]
* JT [SCB_GameDesign]
* Matteo[Loherangrin]
* Mike_C [Amazon]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P. [Amazon]

### Announcement - Matteo - SIG-Release
* Tomorrow we will create the stabilization branch for the next release.
* We will be safe after tomorrow to start the stabilization process.
* We will get the details in the SIG-All channel.

### Announcement - JT
* Monthly Pasadena Meeting Every Thursday
* Soft Launching science fiction short + MPS video game using the same assets
* WE've decided to use workshops to engage the community.  The community stakeholders
  have been wanting to get involved and we don't know how.  Workshops looks like the best way
  with everything else going on, considering everything going on.  I'll work with Naomi
  to get everything started and scaled up.  We'll be talking about it with scale in 2 weeks.
  Workshops are going to be great. 

### Discussion Topic - MPS / WWISE / PopcornFX (Continued again)
* JT: We are going to have to replace the robots and add the new levels and slight encumberment
  for the maxmimo characters and kitbash level, we're not only going to be doing popcorn fx
  we are going to want to replace the assets also in the next year or two.
* Colinb: Two different objects, they happen to be extremely similar.  They are going to go
  on divergent paths here, maybe a fork of the repo would be appropriate?  we can give the object
  a new name, they're still linked, work that goes on one, we can pick over to the other.
  It has an implication on Schema 2.0.
* Decision: Make a branch with latest, and push the branch upstream, call it the PopcornFX-Wwise branch
* Then change main to be miniaudio/OpenParticleSystem.
* We can then add the readme, add it how to readme.md and is discoverable.

### Discussion Topic - Colinb @ Opensource projects
* Showcase - O3DE Pilot - standalone replacement for Project Manager
  * Direciton I'm thinking of for schema 2.0 and how that stuff should all work together.
  * AI Enabled application - does everything that Programe (Project manager) should so, but for schema 2.0
  * UPgrader for schemas in there, AI assistant that you can type to etc.
  * Not fully functional yet but it works, as far as the AI goes.  You can tell it to create a proejct or gem
    and it will do it.
  * Interesting, and I've put it out there so that its still in my repo,in byrcolon GitHub.  Eventually I'll
    submit it for the LF exception and stuff.  Take a look and contribute if you'd like, know that is it very
    bound for LF if they want it.
* SHowcase - O3DE Argus - AI Issue Agent - for Gitlab or Github repo, VSCode extension.  So its on the 
  VSCode Extension store already.  It watches repos, it uses your account to respond to issues, comments, 
  and all sorts of stuff.  For example, if Argus is watching a repo - so if for xample its watching itself,
  and O3DE-pilot, so you can put an issue like "The microphone button does not seem to work" bug.  The AI
  will look at that, see the issue, see if it can confirm that this is an actual issue.  It does all sorts
  of security stuff for prompt injections, etc, once it passes with a high degree of certainty that your issue
  is probably real.  It will start to look at the code and see if it can confirm what you are saying.
  If it can confirm what you are saying it will attempt to code a PR that will resolve the issue.  It puts
  it up there and lets people look at it, and the AI will pick that up and do more work.  Its all crypto-hashed
  and it knows exactly who said what, eg, it said vs someone else spoofing, or trying to trick the AI into
  doing something it shoudl do.  It tries to help you out.  
    * It never merges or anything like that.  It can't actually hurt anything.
* does chain of reasoning on existing PRs, doesn't post duplicates, etc.
* It also scores the different people (or arguses) posting their own pull requests to fix an issue, it looks
  at the pull requests and scores them.  It will figure out which is the better issue / pull request, and if
  its significantly better, or one is incorrect vs, the other ones, or one is a security issue that the other
  one didn't see, it will create a super pull request that incorporates the best elements of all of them into
  one pull request, and score that against the others.
