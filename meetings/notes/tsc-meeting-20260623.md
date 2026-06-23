# TSC Meeting - 6/23/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Andre L.A.
* JTc[SCB_GameDesign]
* Matteo [Loherangrin]
* Nick_L
* Reece H. [DrogonMar]
* Steve P [Amazon]

### Discussion - License Link
* We will accept the licence link PR.

### Discussion - Whitebox additions + Manifold
* It uses a new 3rd Party library (Manifold) Apache 2.0
* Standard in other game engines (Manifold), so having it in our engine can be great for parity of features.

### Discussion - Destruction of entities
* Matteo: It might be worth moving destruction to entire hierarchies always.
* Matteo: Perhaps destroy can be deprecated, and make DestroyAllEntitiesAndChildren can be Destroy?
* Maybe DestroyAndDetachChildren + Destroy

### Discussion - Wayland reset
* Steve P : Wayland package was promoted, and included wayland private headers, so gives you a big warning
* I did an update that suppresses the warning.
* Reece H: If you dont have wayland enabled for AzFramework, it uses XCB as a fallback, and it means the
  fallback is working.

### Discussion - Debug symbols on 3p libraries
* It'd be nice to have debug symbols, windows force-ships with them which makes the files huge, wheras
  linux strips them entirely, which makes it impossible to see stack information (on 3rd party libraries.)
