# TSC meeting - 2022-03-22

## Attendees

Tobias Alexander Franke
Karl Berg
Phil Keslin
Roddie Kieley
Nick Lawson
Jeremy Ong

## [Feature Grid Content Category Clarity](https://github.com/o3de/tsc/issues/22#issuecomment-1075248862)

It wasn't clear whether "content" referred to sample/test content, UX content, etc. Clarity is needed to indicate that "content" refers to expected stability as experienced by the content creator.

Action: Jeremy to submit PR with clarifications above

## [Feature Grid Code/API Clarity](https://github.com/o3de/tsc/issues/22#issuecomment-1075248862)

The various labels for each feature in the Code/API stability section aren't mutually exclusive, and lead to unproductive debates about label assignment.
"Experimental" and "volatile" are seens as overlapping, and "unproven" is being used in different ways across the different sigs.

Suggested set of labels:

- Deprecated (aka, don't use this if you aren't already, and invest time in migrating away if possible)
- Prototype (exploratory feature)
- Evolving (system is operational, but many changes are in-flight which may affect forwards or backwards compatibility)
- Stable (system is operational and production ready)

It was also expressed that many systems would likely receive the "evolving" label, which is appropriate for the project given its lifecycle.

Action: Discuss proposed changes at joint meeting next week

## [Mixamo Collaboration](https://github.com/o3de/tsc/issues/22#issuecomment-1068974416)

The content sig would like to use a Mixamo asset (rig/blend-graph/character) to kickstart O3DE usage, but would need to coordinate with Adobe to see if an exception could be made to provide an open source asset without the existing Mixamo license restrictions.

TSC suggests engaging Adobe to explore the collaboration opportunity. It'd be great to have a robust mannequin that members of the community could use.

## Miscellaneous

### SIG office hours

A request was made to explore the option of hosting sig "office hours" on some cadence to answer questions from the community. These hours would function effectively as times community members could convene to discuss topics without a set agenda. The goal would be to help onboarding community members and involve partners more. No objections from the TSC in pursuing this, but suggested soliciting feedback from sig owners to ensure there is bandwidth.

### Code Reviews

(TAF) There were two concerns raised regarding the current PR process:

1. Code reviews are often performed and closed out by employees of the PR originator, limiting partner exposure to the PR
2. There are issues with CR timeliness (PR is closed before others get a chance to review, or PR is left in the queue for too long without a review)

Time needs to be allocated to a future meeting to resolve these issues. One suggestion was to pursue a tighter "code ownership" model to ensure interested parties are notified to get appropriate PR exposure. One possible tool to facilitate this is Github's [Code Owners](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners) tool.