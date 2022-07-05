# TSC Meeting 2022-07-05 Notes

## Attendees

- Jeremy Ong
- Nick Lawson
- Roddie Kieley
- Royal O'Brien
- Tobias Alexander Franke

- byrcolin[Amazon]
- Finite_State[Amazon]
- galibzon[Amazon]
- geds_dm[Amazon]
- Terry[Amazon]


## [Agenda](https://github.com/o3de/tsc/issues/38)

### Feature Label Requests

_From user dg211_

- Is the TSC required for every label creation request?
-- Yes, because it impacts all SIGs
- How many labels is too many labels?
-- Have ~180 now, but useful in different combinations to filter issues
-- No perceived drawback to having more separate labels as long as addition passed through the TSC to reduce overlap and disambiguate if required
- feature/cloth and feature/destruction had no objections but already been added externally
- Do we have a workflow or process defined for that?
-- No, but a new label request should be made to the TSC for coordination across SIGs
-- New process of creating a new label submit as topic to tsc agenda for discussion
--- List name of it, short explanation and what it's used for
--- tsc make decision
-- Subsequent notification via mailing list and discord
- *Action* @RoddieKieley [RedHat] to e-mail o3de-chairs mailing list to communicate the above
- "This is a temporary label that will be removed once data conversion is complete"
-- WF[1..10] sig-ui-ux RTE related labels for issue workflow grouping and tracking
--- Label deduplication is explicitly outside the duties of the TSC
- *Action* @Royal OBrien [LF] to e-mail to sig-ui-ux regarding label clarification
- Labels for issue sizing discussed and were viewed as appropriate and consistent with other open source projects


## Emergent Discussion

royal: there's a good chance we'll get animation/content from Adobe that we can include in the o3de repo
@galibzon: will the character include animations
royal: yea that's the idea, the character will be batteries included

royal: the group from KitBash is willing to contribute CC-NC licensed content as well
nick: we need to ensure people don't inadvertently use it in commercial content
@byrcolin: we need to put it in a separate repo
royal: yup it will be in the sample repos

royal: I've been working on finding an open source solution for audio, just for awareness
discussion about audio libraries (mention of soloud, amplitude, the soloud plugin, and miniaudio)
nick: the thing about audio libraries is that the backend is just one piece, the tooling is a bigger part (visualizers, graph based audio design, mixing, etc.)
@byrcolin: we can hook the soloud plugin to the external gem system when that comes online

nick: popcornfx is another thing to consider (OSS solution for FX needed)
royal: working with popcornfx to have an OSS option with limited functionality
nick: at the moment they only have various commercial licenses
royal: note that there is a separate license for the popcornfx o3de license (https://www.popcornfx.com/terms-and-conditions/#O3DEPlugin)


## Detailed discussion log

nick: is the TSC needed for every label creation request?
roddie: we need to prevent a label explosion
nick: aren't we already in that scenario?
royal: we have 180 labels, they are used in automation/scripting. we can see what's in use and not in use per label as well and prune unneeded ones. TSC approval is needed because labels impact all sigs.
nick: why would a label explosion be an issue?
royal: we still need to prevent deduplication
jeremy: should we create a process for new labels
nick: the other proposed labels for inverse kinematics and ragdoll seem sensible
jeremy: we'd need to ensure the simulation sig knew to include those labels in their triage process though
nick: yea the sig need for a label needs to start the process
roddie: what would a process for the label approval process look like?
royal: for workflow, a message needs to be sent out to all sig chairs is to submit it as a topic to the TSC agenda with an explanation
nick: is there a mailing list to target all chairs? (yes, o3de-chairs, Royal)
roddie: I can take it as a work item to broadcast that messaging
@byrcolin: a number of issue labels there appear to be removable
@terry: those issues are RTE related
@byrcolin: also a number of T-shirt size labels
royal: we should be using those to size up tasks to be honest. The other RTE issues though need to be better defined by sig-ui-ux
royal to follow up with sig-ui-ux regarding those labels (message sent)

