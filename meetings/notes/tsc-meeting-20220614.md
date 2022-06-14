# TSC Meeting 2022-06-14 Notes

## Attendees

- Karl Berg
- Laura Reznikov
- Nick Lawson
- Jeremy Ong
- Tobias Alexander Franke

## [New PR Template Proposal](https://github.com/o3de/o3de/pull/9912)

- The new PR template is designed to mitigate PR churn due to non-descriptive PRs
- Mention that the process might dissuade contribution if it gets too heavy
- Suggestion to simply the template (remove "Relevant Links" and "Checklist" section, while keeping the link to contributor guidelines)

## [Defining SLAs for security issues](https://github.com/o3de/sig-security/discussions/44)

- No discussion but PSA offered that a proposal for SLA times is on deck from sig-security

## [Docs proposal for SIG awareness](https://docs.google.com/document/d/1Uuz0mvEOMcXBAzcJpop7EqFGzbU2nhXK52wG_c_ls08/edit)

- User Finchy described a discoverability problem for new community members with the SIG process and participation
- SIGs are currently described in [this page](https://github.com/o3de/community/blob/main/CONTRIBUTING.md)
- However, the main contribution website [here](https://www.o3de.org/docs/contributing/) describes the technical aspects of contribution without making mention of SIG participation
- It was suggested that the changes be proposed to the docs SIG directly
- It was also mentioned that ideally, any changes to the docs site would somehow be synchronized with the community repo so there was a single source of truth to maintain

## External Gems Discussion

- User byrcolin brought up an upcoming sig-core concern regarding the hosting, testing, and organization of gems within and outside of the O3DE org
- Gems occupy several categories:
  - Core gems that almost all users will want
  - Extra gems that are more niche, but are vendor and platform neutral
  - Gems that many users will want that are _not_ vendor or platform neutral
  - Niche gems that are _not_ vendor or platform neutral
- The goal is to eventually move all vendor and platform dependent gems to external partner orgs, but a transition period will be needed
- Gems hosted outside of the org will require their own governance and separate testing mechanism, not tied to O3DE's mechanisms
- A proposal is needed to understand the ramifications for any changes to the existing code structure, to be defined, proposed, and accepted by sig-core
- The TSC's involvement will be necessary to handle issues pertaining to funding, process changes, or over project changes that involve multiple sigs
- There was consensus that the project will not scale operating as a pure monorepo into perpetuity, although the exact mechanics for how the project will subdivide over time remains to be determined
- A future memo to the community may be needed to change operating procedures and code discipline needed for versioning, compatibility, ABI matters, and more