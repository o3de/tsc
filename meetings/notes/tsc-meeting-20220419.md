# TSC meeting - 2022-04-19

## Attendees

- Tobias Alexander Franke
- Karl Berg
- Phil Keslin
- Roddie Kieley
- Royal O'Brien
- Jeremy Ong
- Laura Reznikov

## Sig-simulation

TSC has voted to proceed with the formation of the Simulation SIG.

## [RTXGI code sharing update](https://github.com/o3de/tsc/issues/27#issuecomment-1102744595)

User galibzon (sig-graphics-audio chair) presented an update on the status of the following work items:

- Work still needed to move GI to a separate gem
- As a separate gem, conversations with NVIDIA are ongoing to determine gem visibility so external partners can collaborate

Action items: Expect update from NVIDIA meeting in 2 weeks, Galib and Royal to connect.

## [Mac Server](https://github.com/o3de/tsc/issues/27#issuecomment-1101873140)

A question was raised about whether Mac server builds should be supported.
A concern was raised that support without AR is cosmetic.
The counterpoint is that the Mac editor builds are at least unofficially supported, so the Mac server should be user-enableable using the same mechanisms.

## [MacOS AR](https://github.com/o3de/tsc/issues/27#issuecomment-1101881244)

Apple would like to start contributing to the Metal RHI layer soon, but lack of Mac testing and building in AR would likely cause too much development churn.

The primary concerns here are cost and AR run-time impact. A set of proposals would need to be drafted and presented by sig-build so that the TSC can weigh fiscal costs and impact to developer workflows.
Several mechanisms may work to get an intermediate solution (e.g. running Mac AR at a lower cadence, or manually triggered on a PR-by-PR basis).

Action items: Galib to coordinate plan with sig-build
