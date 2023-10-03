tsc-meeting-20231003.md

# TSC Meeting - 10/03/2023 

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L 
* Geds-dm [Amazon]
* RoddieKieley [Red Hat]

## Agenda Items
https://github.com/o3de/tsc/issues/97

This is a regular TSC meeting.  No agenda items were added.

Ad-hoc discussion, script-only.

* Monolithic and non-monolitic installer could be possible.

The problem is the size of the installer.

Discussion on installer size
- SDFormat library.  Build with release and debug symbols, then detach the debug symbols from the shared library
files, so that on linux we have a release library with seperate.
* We should seperate debug symbols out!
* Size is mainly due to template explosions and shared core libraries.

* typeinfo can do function overloading now, insteade of templates.

Export project scripts
- can copy the project.json

* Need to add a button or something to the o3de editor to export the project.  But work needs to be done and is planned...

* Need to be able to include levels in gems somehow, as a demo.  
* Its just a prefab so can probably just include a prefab.

* geds-dm  helpfully supplied links to code locations inside sig-core.
