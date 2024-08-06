# TSC Meeting - 08/06/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Jan Hanca [Robotec.AI]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Lloyd T. [Carbonated]
* Luis Sempé
* nick_l
* null [meta]
* Sid_Moudgil [Amazon]
* Steve P [Amazno]

## Agenda items (official)
Agenda Topic: https://github.com/o3de/tsc/issues/135

(No topics logged)

## Announcements / Topics to discuss while everyone is here

### Announcement/Topic - Joe - Testing
* Joe is asking everyone to test the preview for 24.09 - As of today, no more new features into 24.09 without release approval
* Fixes are still okay.  We'll lock down for fixes in September.  Everything will require an exception.
* Joe Is working on instructions for integrations the other way.  I'll need someone to review it and see how it looks.  I ended up super busy at siggraph so that didn't get done.
* colinb[APMG]
* Joe:  trying to plan for a specific date to test on.  Hard to nail those down since I am travelling a lot throughout the rest of the year, if anyone has suggestions, and how to message this, basically scheduling playtests, so that on a certain day there's a concerted effort to test it.
* Have a tag, call it like, playtest2409
* We'll still keep fixing bugs


## Discussion / Lower Priority

### Siggraph - Joe
* I'll be posting a synopsis about what I learned at siggraph, people who are interested, things we need to focus on (open USD), I'll be putting together a group of people to discuss moving forward with open USD.  We're putting in an assimp USD import, so we can put that in and test it.  But I'd like us to have a plan for the next TAC/TSC meeting to put on the agenda, and see how we're going to implement the USD.  In siggraph, it became very clear that no matter how people feel about USD instead of glTF, every lead in every company is insists on using USD.  There are multiple multi-day tracks on USD at siggraph.  
* Talks all boiled down to "we can't consider it until there is USD support".
* JT: ASWF side can validate what Joe said.  The movement is massive, there is something similar on the ASWF side.  The OpenUSD was generated from USD working group from ASWF.
* Joe: We can work closer with ASWF to implement our USD support.
* Sid_Moudgil [Amzn] - Updating the Assimp gives us USD import.  We would treat it like other data files just like USD.
* Gene is working on assimp upgrading, and someone added a big USD importer to it.  Its the easiest and safest support.
* Joe:  All we need right now is usd support, importing, what Gene is doing works for 2024.  However, longer term wise will need a multi-year plan for how to get USD / OpenUSD to be a native feature of O3DE.

### O3DE Connect - Naomi - O3DEC is next week
* Galib will be talking his talk from siggraph.

### Mascot question
* Trademarks is getting back to us about viable options, soon as they're done with that, we'll sent out a blog that summarizes, and run a survey for 1 or 2 weeks.  
* Many of the submissions were not viable due to legal, community standards, etc, reasons.  But some were good.
* Joe is getting a lot of comments about how boring the logo is

### Release question
* colinb: Do we get a new image for the startup?
* joe:  my goal is ... (if we can't do it we cant') ... but short answer, yes, we want a new image thats more about gaming.
* Joe: What we choose, I'm learning, needs to go thru 2 or 3 point releases as well.  Choose inclusive as o3de, not just games, not just robotics.
* Joe: Accelerated timeline is due to getting approvals, then get draft splash screen, hopefully someone with art skills.  I'll reach out.



