# TSC Meeting - 6/25/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Adam dabrowski
* Guthrie [Amazon]
* Joe Bryant [O3DF]
* Lloyd T [Carbonated]
* Mike S [Carbonated]
* Naomi Washington [LF]
* Nick_L
* null [meta]
* Sid_Moudgil [Amazon]
* Steve_P [Amazon]

## Agenda items
https://github.com/o3de/tsc/issues/130

### Agenda Item (Official) - Tobias - Need Maintainer rights for Joerg Mueller
* Joe:  SIGs make that decision, not us as part of the TSC
* Response would be : Identify the sig that this person works the most with, they can help (the sig chairs) can help guid them thru the process
  of becoming a reviewer and then a maintainer.
* Also for security reasons, teh sigs are in tune with their contributions compared to TSC.
* Put a comment in - link the issue

### Agenda Item (Ad-hoc) - Joe - Data updates
* Sid_Moudgil was able to get most of the assets for most of the lumberyard demos including startergame open sourced.
* Repos are getting up for them.  one for each set of assets.  hopefully before friday. 
* The Assets are in lumberyard format, not O3DE format.  Contributors would need to convert that.  one is already doing that for startergame.  A few other demos people might be interested in.

### Agenda Items (Ad-hoc) - Naomi - O3DE Mascot
* O3DE Mascot contest continues.  At first we were going to limit it to discord/mailing, but we'll start promoting this on socials.  Sketch on a napkin is okay, take a pic, upload it.  Use our creative services dept to polish it. Have people vote, we want it to be a very inclusive event.  
* We're hoping to close this on July 12th, if we don't get enough submissions I'll extend it.  As of right now its still open.  
* Joe: The goal is to get the avatar figured out before release so that the release will contain the avatar as part of the advertising content and so on.
* JOe:  If you're wondering why we are investing in this avatar, the feedbakc we've gotten so far is that our logo is too clinical so far and is too large-corporate-presence rather than a creative product.  o3DE is a creative product and we want to get some more interest in that.  It helps include the community, to appear not as clinical. Most open sources have a mascot - linux penguin, redhat fedora.
* null: Want a character or object that will represent the engine.  it will be included in our advertising, marketing, etc, any time we talk about O3DE.  

### Agenda Items (Ad-hoc) - Joe - conference AWE
* Most people were completely unaware of O3DE
* It was good to learn where the industry is at for AR/VR/XR.  Frustrations people have with the prominent players in that space.
* Meta and Magic Leap were pretty tied in the hardware they used.  Nobody mentioned Apple.
* I was surprised by how much enterprise penetration Magic Leap has.
* No licencing was attractive.
* One customer was paying 6k per developer per year.  They really want to get out from under that.
* Several companies are doing backends for the Metaverse.  RP1 in particular interested in O3DE.  ("Ready Player 1")  They were very interested because they need to upgrade their renderer, they don't want to use Unity or Unreal, due to license.  Giving O3DE a serious look for their frontend.
* Kronos group is assigning us a Liason.
* Kabana group specializes in OpenXR OpenSource implementations. They implemented OpenXR in Godot.  they were going to be looking at our OpenXR implementation.  We have Galib who is working on it, but they wanted to review it, do work inside O3DE to help get our OpenXR up to par, etc.
* With AWE, among enterprise they were surprised we exist, but happy we exist due to the open licensing, and they can contribute for what they need.  our visibility is just so low still.  Me going to these events, my primary responsibility is raising the visibility of o3de.  Going to to siggraph, Galib is giving a presentation - it should help with visibility.  "Hey, we exist, take a look."

### Agenda Items (Ad-hoc) - Naomi - SIG-Docs update
* In progress attempt to spin back up the docs WG.
* Meeting prior to last week.  they have decided on every otehr wednesday at 11am ET.
* Anyone who wants to take part in the docs WG, its happening.

### Agenda Items (Ad-hoc) - Joe - Project Life Cycle doc?
* TSC - Have you had a chance to look at the current project life cycle?
* Nick: Yes, added comments.
* Naomi: The TAC Meetings are open to Everyone.  Nick and Sid are our TSC Chair and AWS technical rep respectively.
* Joe: We have 3 potential joiners to our foundation.  Lot of interest has been in joining our foundation.  Which is awesome.  There are benefits to us (Visibility across the board, more chances of funding, join as members, ...) initially there are downsids in that our existing funding has to get these projects up and running.

### Agenda Items (Ad-hoc) - Nick 
* Update on Asset importing
* Joe:  we need someone to maintain EmotionFX.
* Joe:  Everything else is maturing and maintaining around EmotionFX but not updating EmotionFX
* Joe:  we don't know what to test or internals / what to do when something breaks.
* Mike S. - This is a prickly issue.
* Multiplayer Sample is not sufficient as a smoke test?
* Joe:  It doesn't exercise a lot of the features, just the bare necessities.
* Joe:  I did try to reach out to the primary authors, they are not allwoed to touch or talk about it due ot their current employment.
* Joe:  we have 1 other person who does not work for epic and I'm reaching out to them.
* Joe:  he's at a game studio but its not considered a competition issue.
* Joe:  One more (Chris).  He worked on that quite a bit.  
* Joe:  I can follow up.
