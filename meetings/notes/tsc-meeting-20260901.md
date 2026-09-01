# TSC Meeting - 9/1/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* ChristianHinkle
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* hex
* Jan Hanca [Robotec.ai]
* jayrulez
* JTc[SCB_GameDesign]
* Mike_C
* Nick_L
* Reece H. [DrogonMar]
* RoddieKieley [Red Hat]
* Steve P [Amazon]

### Announcement - Jan Hanca [Robotec.ai]
* https://github.com/o3de/sig-release/pull/374 - Release process for canonical repositories in between official releases
* https://github.com/jhanca-robotecai/sig-release/blob/d81b8834ab33ab959aa4b3fb1e35a4da73072207/releases/Process/Intermediate%20Release%20Process.md
* https://github.com/jhanca-robotecai/sig-release/blob/d81b8834ab33ab959aa4b3fb1e35a4da73072207/releases/Process/Major%20Release%20Process.md

### Announcement - Mike_C [Amazon]
* Asking LF for mac signing certs.  hopefully, we get some things going soon.
* If we do want to start signing, we will find a way to do so that is safe.
* Nick: Are we still going to be using the jenkins?
* Mike: This last time.

### Announcment - JTc - TSC Meeting Notes from outreach committee
 * https://discord.com/channels/805939474655346758/1544352419205615719

### Announcement - Jan Hanca - O3DE Extras
* Jenkins was failing and so we didn't have any tests in o3de-extras
* Drafted a GITHUB Actions, and it was reviewed and I asked co-pilot to double check
* If anyone wants to have a look .   Its only for simulation gems.  I posted a link:  https://github.com/o3de/o3de-extras/pull/1089
* Sim Gems only work on linux with ros2 being installed, so I keep it separately.  Its better to have tests than not having tests.
* Mike_C [Amazon] - Nightly Development Jenkins is still running
* colinb[APMG] - Schema 2 being iterated on.  I was reading on what google does (copybara) - they try to solve what our issues are
  internally and externally.  Monorepo for git commits across the repo, however, that's for development.  for consumption, putting
  it out externally, they do what I was doing, schema 2 sneak peek style, you chickenate, the monorepo gets choppsed up into smaller
  repos and externally available.  I'm integrating that into the next iteration.
* You can use the 'chickenated' repo to interact.  The code goes up to the mono repo.  Sort of like a fork thing.
* https://github.com/google/copybara

### Discussion - mimalloc
* slight performance increase - work continues

### Discussion - ChristianHinkle - How can I become a reviewer?
* Start reviewing on your own, ask your TSC, if you're already involved (PRs, reviews, issues, etc) then its even easier.
* Arbiter: Some of the more recent PRs are AI generated.  They are massive, have the prompts, etc.  They take a lot of time to look over.
* Mike_C: Be honest where the source code came from.  Did they generate it or not?  ARe they taking responsibility for that code.
  If it is a huge refactor, request that they break it up into digestible chunks.  You still have the human at the end of the chain.
