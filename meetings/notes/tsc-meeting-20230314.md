# TSC Meeting - 3/7/2023

# Chair and Co-Chair
* nick_l[amazon] 
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L [Amazon]
* Tobias Alexander Franke [Huawei]
* geds-dm [Amazon]
* RoddieKieley [Red Hat]
* kberg [Amazon]
* colinb[APMG]#6994

## Agenda Items
https://github.com/o3de/tsc/issues/72

1. label: platform/linux/arm64
2. label: sample / example on the repos

### Platform label

(flowing discussion, many participants.  Will summarize here. TSC Participants: feel free to correct this in Issue!)

* the TSC Discussed several possibilities, including platform/linux/arm64, etc.
* It turns out that the default behavior of Github is to use an "AND", that is searching for 'label:"platform/linux" label:"arch/arm64"' will combine them into one search that includes both.  We may also eventually want to support Mac M1, as well as Windows and other ARM arch implementations, and thus the conclusion was to add the following tag:
* 'arch/arm64'
* Pre-approval was also granted for 'arch/x86_64' if it ever becomes necessary.

### sample topics on repo

(Flowing dicussion, many participants, will summarize here. TSC participants feel free to correct this in Issue!)

* What is the right topic to utilize that allows people to find what they're looking for?
* discussion: The TSC members present had no issue with correctly adding Topics to our repositories.
* we should add "o3de" to all of the existing related repositories that deserve it.
* "sample" seems common.  Label the sample repositories with 'sample'
* use whatever topics make sense, actually.

