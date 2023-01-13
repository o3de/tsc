# TSC Meeting 2022-11-08 Notes

## Attendees

- Karl Berg
- Tobias Franke
- Roddie Kieley
- Nick Lawson
- Royal O'Brien

- byrcolin
- geds-dm

## Agenda - Office Hours

- Expected topics
  - [TSC Chair and Co-Chair Elections](https://github.com/o3de/tsc/issues/62)

## Miscellaneous notes

roddie
- https://github.com/o3de/tsc/issues/62

tobias
- code approved for release
- code for mobile focus

royal
- new project, group doing metaverse work
- starting to build for large customers
- want to ensure that under open standards
- companies are getting open meta experiences built, but not sure of reusableness
- [Open Metaverse Foundation](https://www.openmv.org) setting that framework
- [Open 3D](https://o3de.org) as that open standardization of what we can achive
- [glTF](https://www.khronos.org/gltf/) / [USD](https://graphics.pixar.com/usd/release/index.html) / materials
- putting the strong voice forward for openness

roddie
- [TSC Chair and Co-Chair Elections](https://github.com/o3de/tsc/issues/62)
  - initially announced time has elapsed
  - more contribution would be good

royal
- next steps are to put it out to the members
- state that chair/co-chair in the interim
- if no vote then defer
- either accept or deny
- just point to the [public thread](https://github.com/o3de/tsc/issues/62)
- ppl already casting vote in there
- if no vote, then abstain case

roddie
- office hours today
- any emergent topics?

royal
- through next week start looking at how we start to pull these pieces together
  - standards etc
- how can o3de participate in setting these standards
  - o3de as thought leaders
  - how do we communicate that?

colin
- that is the right way to go about it

royal
- discord, groups io, other things
- questions and focal points, areas to try to solve
- good representation from the o3df
- can anticpate [USD](https://graphics.pixar.com/usd/release/index.html) as a big topic
- will probably see large companies interested
- need good representation from here, already seeing folks want to use o3de
- liaisons, representation not specifically for the company, but as the individual member
- having a voice that brings information
  - saying need 1 or 2 from a given community that can carry the questions in both directions
  - bring it back to the sig for them to then solve
  - anyone can jump over and start talking
  - someone who is watching and communicating then the voice stays present
- e.g., embedded format of a texture should be aligned with the metadata
  - if they can answer or if don't have time they can bring it back to the sig
  - sig can go directly answer or use the liason person
  - make sure they come back into the sig area
  - if no one is watching then no voice or presense
  - person not responsible for everything but bringing it back to the sig

colin
- by default should be sig chair or co-chair, unless they designate someone else

nick
- have to be careful of putting too much work on the shoulders of the chairs

TOPIC for tsc/sig meeting
- sig chair/co-chair representation at the [Open Metaverse Foundation](https://www.openmv.org)

colin
- I volunteer for sig-platform

royal
- once we have representatives
  - not they are the centre knowledge poitn
  - bringing knowledge and awareness back

nick
- barrier to entry and friction for the representatives
  - for folks volunteering time
  - ideal person like colin re: sig-platform chair

royal
- agreed

nick
- finding leaderships for the sig's can already be challenging
- for the metaverse liaison maybe moreso if it isn't something that particular chair/co-char is interested in

royal
- can ask the sig leadership to help find/appoint within the sig's community
  - if not and have time then jump in and help

nick
- e.g. chair of sig ui/ux may only have primary interest
  - [Open Metaverse Foundation](https://www.openmv.org) liason may not be in that interest where volunteering time

royal
- always have to approach it as if no one works for any company
- so if don't want to do it then they won't
- need low enough barrier to entry

colin
- would appreciate any further info on that

royal
- doing this across 6 foundations
- ai voice dncf hyperledger openwallet open3d
  - impacts all 6 [Linux Foundation](linuxfoundation.org) foundations

royal
- ways we can kick-start the mobile working group

tobias
- 1st thing needed is regular meetings

royal
- need chair of that working group

tobias
- have an idea of who we can ask that has a strong interest

royal
- lets start there
- likely all the VR space will want to be involved in mobile
  - thinking SoC's and phones in particular

royal
- another thing that's been wanted to do for a while: o3de certification
  - how can we do a certification
  - linux distros in particular
- how can we be able to say it'll work on this distro or or that distro

nick
- the way that o3de works is different than linux ecosystems
- QT has cusotmizations for example
  - sometimes it has been customized for style

royal
- can we determine how much customization?

nick
- largely around the QT docking system
  - everything was contributed back that was technically possible
- somethings are not hookable
- sometimes not good enough for what you want

nick
- could go hard into containerization

tobias
- flatpak
  - a way where you install without depencies

royal
- put a small discussion on package management
  - QT fork with all of the changes but it's open
  - larger community might not know what you do
  - discussion thread with background as to why going down this road
- open source engine, due to metaverse
  - if we want to use distro's as backend for cloud services
  - have both client and server side
  - usable and operable
  - easy to pick up
- going to see this shift happen over the next 6 months or so
- at least have raised the awareness can help contribute to get it done
- need to raise the awareness to be able to get the community able to do

colin
- on the QT front were the customizations ever contributed back?

nick
- yes, but the docking changes in particular were a bit too much and a bit too big to be accepted at the time
- as the customized QT belongs to o3df now, we could make another attempt

royal
- might be a good idea

nick
- the docking system is cool and really good

colin
- it's a step up from the existing, not sure why they'd say no
- there are other changes too, one around memory was resinded I recall

colin
- might be worthwhile to remove, i.e. build normal QT with minimal changes and see how it functions

nick
- only modified QT base and image formats
  - for TGA RLE support in particular as QT doesn't support that by default
- HiDpi fixes
- will give the commit tree of qt base a diff for curiousity sake

royal
- if we can take some of this stuff and contribute them back if we have these changes 
  - can go back to the QT community
- should have it in our community discussion
- no idea how many ppl are QT devs that love it
- it could help contribute to what we want to do as our strategy

nick
- for other 3rd party dependencies
  - not too much diff
  - may be able to depend the system version directly
  - same qa'd version if flatpak containerized

nick
- existing large containerization effort, [o3tanks](https://github.com/loherangrin/o3tanks)

royal
- [loherangrin](https://github.com/loherangrin) still very active

nick
- found one of the containerized environments pushes LD_PRELOAD which causes compatibility issues between distros

royal
- these are things we can bring to the community to get things prepped;
- at the tsc level to guide the strategies
- regarding the open metaverse, open3d has the best chance to standardize it as a project that is not commercially bound

tobias
- at the mercy of a commercial engine developer

kberg
- on the containerization front, I've been running the engine like that for a while now
- there are a number of technical hurdles that make this difficult at the moment
- for example, what is the configured graphics driver pass through?
  - need efficient passthrough
- at the moment the configuration can be painful at times

