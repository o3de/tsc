# Joint TSC : SIG Meeting 2022-03-29

## Attendees

Joe Bryant (sig-release)
finite_state (sig-docs)
Roddie Kieley (co-chair sig-platform)
lumberyard-employee-dm (co-chair sig-core)
Tony Balandiuk (sig-release)
Stephen Tramer (chair sig-docs)
Yuyi (sig-ui-ux)
Gavin monroe (sig-content)
Sean Sweeney (sig-testing)
Karl Berg (tsc)
Nicholas Lawson (tsc)
Jeremy Ong (tsc)
Royal O'Brien (tsc)

## Sig Direction survey

sig-release
- 2022, 2 releases: 1 in may, 1 in october
- documenting release strategy so that others can perform releases (would like folks outside amazon to be more involved in the process)
- developing long term strategy
- focus on reducing friction in performing releases (emphasis on cross-cutting efforts)

sig-docs
- Automation support (docs written by hand that should be automated)

sig-content
(best guess)
- Issues inbound indicate gaps in the content ingestion pipeline (features)
- Performance issues (asset processing performance, editor perf, runtime)
- Improving documentation to increase external contributors

sig-platform/systems
- Long-term would like to aim for platform parity (aarch64 + x86_64), Mac desktop (M1), mobile (ios/android), Linux (various distros)
- Platform-dependent installation (e.g. with Arch pacman, Debian apt, etc.)

sig-ui-ux
- Rev-the-engine (RTE) program, a data-driven approach to assess workflow quality for various game dev workflows (10 different pipelines assessed)
  - Focus is on development of a "first-playable" demo in O3DE (surveys, working sessions, user-studies will be conducted to evaluate the current state of the engine)
  - Knowledge/feedback will be distilled to the sig
  - April/May current evaluation information coming soon
  - (Speculative?) September timeframe for a game jam to reevaluate improvements made throughout the year
- Community engagement improvements
  - Sharing user testing results with the community
  - Interview specialists from various domains
  - Continue to develop the BlueJay design system
  - biweekly office hours
  - Roadmap transparency on Github
- Areas that need extra attention
  1. Actor-development workflow (animation, attachments, rigging, cloth)
  2. World-building
  3. Multiplayer (untested by external users)

sig-graphics-audio
- Performance improvements (rasterization pipeline, raytracing pipeline, lighting, materials)
- Material canvas
- Artist workflows

sig-core
- Performance improvements
- Reduce dependency on ObjectStream (reflection improvements)
- Allocator refactor (linkage/initialization issues, extensibility)
- Archiving system which is nVME-friendly
- Project workflow improvements
- Spin-off physics/animation into simulation sig

sig-test
- Backlog-planning in progress for improvements to AR/tooling
- Cross-sig communication improvement
- Performance testing automation
- Rollout usage of "Github owners" features to clarify code ownership
- Seeking more external contributors
- Metrics needed to evaluate test stability/flakiness (false positive/negative rates)
- REQUEST: Metrics framework (participation from sig build)
- TIAF followup (on the roadmap, Q2, incremental rollout)

sig-security

sig-build
- Local reproducible builds (many scripts are dependency-heavy, over-reliance on Jenkins)
- Test limitations (Mac, GPU availability, restricted platforms)
- Cost reduction (stability + flaky tests + build perf has direct impact)
- Build performance (asset sharing between builds, ccache/distcache-like functionality)
- CI/CD pipeline continued support
- Documentation
- Cross-cutting issues (supporting other platforms/hardware)
- Investigating containers to run docker/multi-node setups locally
- Cost transparency
