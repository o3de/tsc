# TSC Meeting - 06/10/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* bartlomiej Styczen
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* Matteo [Loherangrin]
* Mike Chang [Amazon]
* Nick_L
* Reece H. [DrogonMar]
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement

### Discussion - Nick - Add OpenMesh
* Can we add OpenMesh?
* Mike: We have permissions to add it.
* Colinb: has a wizard for it.
* Mike: There is a GHA that has a auto mirror continuously sync a gitlab repo.

### Discussion - Nick - Index the vectors
* Check in with Mike B [Amazon] as to why
* Sid is okay with it.

### Discussion - Colinb - Schema 2.0
* To discuss with Nick.
* The way we add a gem, there seems to be a couple ways to do it.
   * Gem Names (project.json)
* Writing an upgrader in schema 2.0 and translates it into the latest way of doing it.
* Changing external_subdirectories to be gems.
* already seperated, external subdirectories, recursed, automatically recursed.
* Schema 2.0 is going to deprecate most of whats in schema 1.0 which was the parent describing its children
* When a gem says it has a dependent gem, its only used by the project manager.
* possible deep future:  remove all of the gems from the engine, and have everything modular.
* A release of the engine would not necessarily mean a release of all its gems, just the repo.
* The engine would be an object just like everything else.
