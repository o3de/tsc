# TSC Meeting - 09/24/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Jan Hanca [Robotec.Ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Naomi Washington [LF]
* Nick_L
* RoddieKieley [Red Hat]
* Sid_MOudgil [Amzn]
* Steve P [Amazon]
* Tobias Alexander Franke

## Agenda items
Agenda Topic: https://github.com/o3de/tsc/issues/141 (no issues)

## Announcements

### Announcements - Joe - sig-release
* Release is coming early october
* Please attend todays' release meeting.  
* I've approved all 5 current exception requests.
* Submit the PR to stabilization if ou have an exception outgoing
* Several companies are using o3de stabilization on a daily basis, so I'm fairly comfortable.

## Topics from Agenda (None)

## Open Discussion

### Discussion: Naomi - Mascot
* Thinking of a name.  Probably Awdie?  Odie is taken (Garfield), Audi is taken (car brand), Atomie (used in various forms).

### Discussion: Colinb - APMG has secured middleware license for XBOX dev
* Sony is tougher, wants a customer.  Chicken/egg problem - they want a customer, but a customer won't exist until the port is available.
* 2409 should make it easier on Switch, android perf and feature work should help.
* Sid_Moudgil: Would need a new backend, NVN, since its nintendo specific renderer.
* Joe:  This week having talks with about using o3de, they asked about o3de console support.

### Discussion: Joe
* I've posted link to project board https://github.com/orgs/o3de/projects/62/views/1
* Talking with community managers, and will talk with JT about some ideas I have about community moderation
* We don't want non-inclusive language, thats one strike you're out if its blatant
* We do give some leeway and chance, but we also want to boot trolls that are only here to be negative, we give warnings, then remove.
* JT: Typical ad-hominem statements are when you attack in a generality or discuss those specific items.  They are veiled by a skilled troll.
* JT: On a side-note, but I've told that godot dumped their entire discord and felt it was overrun and was more serious, more developer based.
* JT: Internally, local people, are incoming next month too, and people are showing interest.  Quite a large training org that is interested in open source as part of their training globally.  This is a big step, they take it seriously.  
* colinb: It should be time based, etc.
* null: You have to be very light handed and subtle about it
* Joe: I'll forward a document to you that shows phases/steps
* null:  Users join the community with a TOS
* Nick:  there are ways to show people a TOS/community guidelines before they get to see the rest of hte server.
* Joe:  we can't be restrictive on speech but there is a line, we can't just be a cesspool of negativity.  we want community members who use the product and are constructive for the community, not those that come in purely to tear it down without offering anything valuable to the community.
* null: I went thru a similar thing with goonsquad / mechwarrior.  Troll the community.  Any moderator activity to remove them became a point of conflict to cause contention with.  the one thing that worked was to call them out publicly.  For example, ask them to clarify, put data behind their statements, it became obvious that their arguments fell down.
* There is a sequence - warning, silence, ban, etc.

### Discussion: JT [SCB_GameDesign]
* 111 Good-First-Issue tags, I would organise with the community and see if there's a way to bring the community together for good-first-issue
* I scanned several pages, some are fixed, its all for onboarding new people, so that's okay.
* I did reverse order of the issues, and I'm still on 2021 and did a reverse order, a lot of it is fixed, a lot of cruft in the repo right now.  3.5k issues open, but a loooooot are fixed already, but not closed.
* Joe:  My first instinct is to burn anything longer than a year old, and it will help us get thru all the cruft and focus on the things that matter right now.  I will need help from the sigs to identify in the last year that its super important.
* We will target the "last correspondence date" so thing that are still being discussed will stay open
* We will send out messaging/marketing first
* The closed message will indicate that the ticket can be reopened if its still affecting you.
* JT: Some projects/sigs/rfcs and have been paused but are still active.  Nobody has picked up.  
* Joe: RFCS immune, its bugs/issues in O3DE.
* Joe: we'll go thru the blocking/criticals first, then check the blocking/criticals but finer grained look at those issues.

### Discussion: Colinb
* Some of the levels pop up a conversion notice when we open it
* We should just re-save it
* Cloth is broken (known)
* Sid:  Sounds like its a development branch fix.  Will require an investigation.
* JT: Good practice is to add prefix/postfix to "test"
* Joe: We need to add the reserve names in the code to add things that could break people.
* Joe: docs front and center, make sure that the docs say not to use certain keywords for the process.
* Nick: we can add the keywords to the code that already checks.

