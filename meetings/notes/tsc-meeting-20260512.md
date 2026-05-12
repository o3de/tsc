# TSC Meeting - 5/5/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Andre L.A.
* Arbiter
* Cheddarspice [iamjbq]
* colinb[APMG]
* Hellaenergy (Nick) [Red Hat]
* JT [SCB_GameDesign]
* jayrulez
* King Shocke
* Mike_C
* Nick_L
* phandradee
* Reece H. [DrogonMar]
* Sid_Moudgil
* Steve P [Amazon]

### Announcement - Nick - SIG-Release
* May 27th new release date

### Discussion - Release number
* We'll go to 2.6.0 most likely for this release
* We'll go to 2.7.0 in dev.
* At some point in the future we'll need to compose packages somehow, based on version number.
* JT: ASWF adopted REZ as a python based package manager.  Still lining things up.
* colinb: We have many objects in a large heirarchy - and people have 2-3 versions of the engine, all the subordinate
  objects have the same version number, it confuses the map and the map starts choosing objects from different places.
* colinb:  Are we going to go into an LTS sort of release type system.  We have long projects like this, 2 years or more
  for a game cycle basically, do we want to LTS?
* colinb: We could have one lts window, which we support for 2 years.  when it ends, next release becomes the new LTS.
  So at minimum its support for 2 years.  Never multi-overlapping LTS.  And then we say that the only updates the LTS gets
  is a security vunerability and major bug thing.

