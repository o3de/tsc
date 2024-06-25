# TSC Meeting - 6/18/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Lloyd T. [Carbonated]
* Mike S. [Carbonated]
* Nick_L
* null [meta]
* RoddieKieley [Red Hat]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Agenda items
https://github.com/o3de/tsc/issues/129

### Agenda Item (Ad-hoc) - colinb- remind to tag PRs with a sig.

### Agenda Item (Ad-hoc) - Lloyd T.
* CVAR registrations - whenever they are called
* Non-monolithic build, the cvar get deferred list and executed
* Monolichic build, they get issued immediately.  This provides an inconsistent flow of logic between monolithic and non-monolithic builds.  This is is done in GHI.
* null: Can we not just always add the cvars to the deferred list.  The CVAR goes into the deferred list until the console list becomes available.  Program startup flow - if we base the flushing of the deferred list to some part of the startup sequence, whatever the same logical point is in startup flow, could we still do that in monolithic build?
* colinb: Some of the cvars are startup process cvars.  So it might load a different object based on a CVAR.
* Sid_Moudgil [Amzn] : we have logic based on command line options or device config, but its not cvar set.  There are some settings registry code there but the issue is the standard cvar issue.  We would just call PerformCommand.
* Is it because we're competing with the CryConsole? (No.  Its due to dlls having a copy of each declared variable)
* New console does not have RCON.
* There's a point where we instantiate the iconsole interface and a place where we load and run all those cfg files.

### Agenda Item (Ad-hoc) - Lloyd T.
* Does the engine support asset references to a known asset type (mesh, texture)
* Not a truly generic type















