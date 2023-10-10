tsc-meeting-20231010.md

# TSC Meeting - 10/10/2023 

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L 
* Geds-dm [Amazon]
* RoddieKieley [Red Hat]
* colinb[APMG]
* Joe Bryant [Amazon]
* null
* naomiwash
* Nicole Hussman [LF]
* Sid_Moudgil [Amazon]

## Agenda Items
https://github.com/o3de/tsc/issues/98

This is a regular TSC meeting.  No agenda items were added.

## Release Status (Topic by Joe Bryant)
* The release went out yesterday, everything looks good so far.  
* No support issues yet (monitoring github, Discord, local testing)
* Naomi: Release notes need to update on Netify.  The one thing thats not updating properly.


## Public meeting tomorrow (Topic by Naomiwash)
* Open forum in Zoom meeting.  No pre-questions yet.  Its a Q&A Session.
* Naomi will be watching the channel and seeing what goes on.
* Sid will be here for graphics questions

## Criteria for Change Acceptance (Topic by Null)
* For changes to accept, we need 2 reviewers.
* Maybe 1 reviewer, if they are the maintainer?
* Graphics side - struggling with the multigpu work that Huawei is doing.  Because they are a sepearate company, they are focused
  on their own platform - PC, vulkan, etc.  When yhou're changing a lot of code, dramatically ,their bar was much lower at the start.
  Its taken 6-7 months to get to undertand the acceptance.  I rejected it and we're going thru the process of breaking it up to PR
  in smaller pieces... every 3 days there are more PRs and theres just 2 of us doing this.
* 3 Engineers from Huawei know RHI very well.  We are trying to get reviewers into the maintainers list that have the necessary expertise.
  They just want the O3DE to work on multi-gpus probably on cloud nodes.  Mobile and other platforms are less important.
* Mac is not an officially supported platform.  Basic pieces supported for IOS.
* We prioritize windows and linux, IOS and Android above mac.
* Decisions like this are made at the TSC level.
* SIGs are really inactive and chairs.  We should try a RFC, comment on this, etc.

## Side discussion on sigs not having chairs/co-chairs
* One option is to wind the sigs down until needed again...
* One option - Contributing sigs (Contributing code) - we can focus on them more
* One option - combining sigs (TSC not aligned with this option)
* Start a GithubComments thread on different sigs.  One would be discord channels, perhaps a google doc?  Get opinions.

## Related topic:  Audit of current maintainers/reviewers
* Maybe we should remove maintainers that don't fit the criteria.


## Action itme: 
Suggest a motion to remove the rule that a chair can only be over one sig, in an interim.
Tag the TSC-voting members.

