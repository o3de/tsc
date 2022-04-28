# Joint TSC : SIG Meeting 2022-03-29

## Attendees

Joe Bryant (sig-release)
Roddie Kieley (co-chair sig-platform)
Tony Balandiuk (sig-release)
Stephen Tramer (chair sig-docs)
Sean Sweeney (sig-testing)
Karl Berg (tsc)
Tobias Alexander Franke (tsc)
Jeremy Ong (tsc)
Royal O'Brien (tsc)

## RFC Feedback

There was some discussion about the RFC process, and the main point of
discussion was about increasing visibility of RFCs. The TSC will discuss
at a future meeting amending the existing process to leverage the existing
RFC repo as an index of published and pending RFCs that the community can
quickly peruse.

## Upcoming release

Release is on schedule with release notes set to be compiled on 2022-04-29
and code lock set for 2022-04-28. There are 11 pending stabilization issues
as of this writing. The branding update is required for the release.

It was suggested that sig chairs and co-chairs proofread the "feature grid"
entries in the repo prior to code lock so that the docs sig can cut the
features and stabilization data present.

## Working Group Discussion

A reminder was issued about the process for creating a working group (WG) and
the situations that would warrant WG formation (generally, cross cutting problems
that warrant the fixed overhead of forming the WG, to reduce the total operational
overhead of coordinating across sigs).

The main candidate for forming a WG at present is VR support to the engine. M-GPU
support was called out as an initiative that is largely in the domain of sig-graphics-audio
and would not generally warrant the formation of a WG. A charter/document is needed
to describe the function of a hypothetical VR WG, to be presented at a future meeting.

## Sig Meetings Discussion

Sig chairs and co-chairs were informally polled about their meeting cadence and
productivity. Sig-graphics-audio presented an experimental change to have more regular
"general purpose" meetings and relegate issue triage specifically to another day in
the week, with the goal of having a general meeting less encumbered by strictly
process-oriented matters.

UX mentioned having some success holding office hours weekly, although it was mentioned
that time conflicts between various meetings within O3DE is posing an attendance problem.

## Recast-navigation approval

TSC did not have quorum to officially approve Recast/Detour as 3P libraries, but
the libraries were discussed and there were no general disagreements about its usage.
This will be discussed at a future meeting.