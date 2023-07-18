# TSC Meeting - 7/18/2023

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L 
* geds-dm [Amazon]
* Naomiwash
* Nicolas [Red Hat]
* berry
* RoddieKieley [Red Hat]
* Royal OBrien [LF]
* drakeredwind01 [cyber-sec, idea]

## Agenda Items
https://github.com/o3de/tsc/issues/88

### Miniaudio
* MiniAudio gem got a PR that made it more compatible with O3DE licensing requirements.

### The feature grid
Royal is working on upgrading the feature grid export feature, expects it to be ready for next release.
The idea is that when the stabilization branch is captured (and thus the features are locked), we generate the feature grid
at that point and snapshot it for the future release and that doing so is a 1-click.

### Naomi
Presented https://docs.google.com/document/d/1b-g1tAjDwMmEBzGBZ34OBTlBk-InUWxNzUqLJI-uNkg/edit (from previous meeting)
The document outlines the suggested way to run and manage SIGs.
It is a working doc and can have changes be made.

Question was whether it should be published and where?
- current TSC members present are in agreement, yes, and put it on the wiki.
- put it in o3de/o3de and link it from the other sig wikis or front pages
- add a high level description of this document being a living document and encourage suggestions and changes.


### UX DOC
* Onboarding is one of the top pain points but also one of the least contributed areas.  It may be the case that the corporations
or studios making games see it as something they need to invest in (since they go thru the pain of onboarding and then solve it for themselves and move on to make a game).
* geds-dm brings up robotics community + plugins, and so on.
* Need to focus on making it easier and easier to get in and get started
* Indie game developer - berry - talked about the onboarding issue. Berry had a rough time onboarding after coming from godot.
>   asked for help for discord.
>   told to run old version installer, couldn't get the editor working.
>   Errors showing up, big turnoff, if the engine is super easy to install it would get more people to use it.
>   Lack of tutorials on youtube.  I would make tutorials but if I could not get it installed, this is a huge filter/problem/isuse.
>   If I had no problems installing the engine I could spend my time to learn it.

Maybe we could have a default project (without a DLL?) or make it so that its possible to make dll-less projects and still be able
to export it?
Started a thread
https://discord.com/channels/805939474655346758/1130890008098783343

