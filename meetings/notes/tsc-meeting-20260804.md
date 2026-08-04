# TSC Meeting - 7/28/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* colinb[APMG]
* Jan Hanca [Robotec.ai]
* JTc[SCB_GameDesign]
* Nick_L
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Steve P [Amazon]

### Announcement - none
 
### Discussion - Arbiter - RFCs changed locally other people might want?
* Working on RFCs 
* Dissolving atom
* bumping c++ base to c++23
* bumping AVX baseline for x86 processors
* colinb to check the platforms we care about and see what c++23 support might close down
* We might want to use ISPC

### Discussion - colinb - composing workspaces and o3de schema 2.0
* Asking about previewing the schema 2.0 system.
* Maybe we do 2.0 in parallel to 1.0

### Discussion - colinb - SHINE vs LYSHINE
* We need a branch containing just the renames (as a commit) and then a PR targetting that branch that has the slice -> prefab changes
  to review.

### Discussion - arbiter - schema2.0
* We heavily lean into monorepo.
* colinb: You could try  https://github.com/accesspointmg/o3de-pilot - and give it a try see what feedback you can give.
* O3DE Pilot gets everything you need locally to constuct a workspace for you, and even build it for you, if you tell it to.

