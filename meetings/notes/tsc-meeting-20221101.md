# TSC Meeting 2022-11-01 Notes

## Attendees

- Karl Berg
- Tobias Franke
- Roddie Kieley
- Nick Lawson
- Royal O'Brien
- Jeremy Ong

- Aaron Ruiz
- byrcolin
- Chanelle
- Danilo
- geds-dm
- Raegan Brown
- Razlken

## [Agenda](https://github.com/o3de/tsc/issues/55)

- Continued, as last week it was noted that many Amazon based members were out due to an annual learning event and as such the discussion and regarding the mobile effort was moved forward.

### Establishing the path forward for Mobile

- briefly mentioned commentary already on the [#46 discussion thread](https://github.com/o3de/tsc/discussions/46)
- recalled the e-mail as sent out to invite participation at this meeting to help establish the path forward for mobile focused efforts
- to help frame the discussion the questions of what belongs to the effort and therefore what no longer resides where it is were asked
- it was noted that at the moment there is not a specific sig-pc, for example, and that a sig-mobile would set a precedent
  - would need to be cognizant of what this would mean wrt to how groups would work together
- was it to operate like a hub? where issues were pushed out or would expertise be pulled in?

- a number of concerns had been raised at [O3DCon](https://events.linuxfoundation.org/o3dcon/) related to the need for a mobile specific focus
  - optimizing the graphics
  - optimizing the speed and size of the execution
  - standardizing the api

- followup discussion occurred around what the specific initial device targets, mobile o/s, and graphics api 
  - mobile alone a too broad target to start with
  - tablets and handhelds, i.e. phones with specific models being prioritized
  - while more input was recommended from those involved, ideally *NOT* OpenGL ES 
    - although mobile Vulkan coverage is far from complete
  - in the future HMD's to also fit for AR/MR/VR

- with respect to optimizations
  - need some in the areas of sig-core
  - need some in the areas of sig-graphics
  - but binary size and performance alone are not the only concerns
  - i.e. the focus areas that are important for mobile are specific
  - console similar, e.g. targeting from PS5 to Switch requires specific knowledge, tools, and optimization techniques

- as the work covered existing areas, the question was asked as to what prevents the work from occurring within the existing structures
- what would an ideal workflow look like?
- what resources are really required to allow the work to proceed?
- if a sig was setup now to accelerate the work, what about the longer term workflow impact?
  - e.g. work on atom to have more input sizes also would impact sig-graphics in general and other platforms
- maybe the workflow is a good fit for a working group

- related to the working group versus sig question
  - it was noted that the original request was that of a working group
  - the charter as laid out at the moment was not as mobile specific as expected
  - for the mobile work need to be careful that other platforms are considered as all have to work and move forward together
  - would be harder to unform a sig given working groups are meant to have a more fixed and definitive lifespan
  - working specifically per platform or generally
    - it was noted that there was previous experience in doing a single thing eight different ways rather than doing the one thing a single way across platforms
    - short term velocity but low cohesion for the case of doing the single thing specifically eight different ways
  - either way would be complex without a group focused on mobile
  - timeliness question
    - would we ever see the working group disassembled? mobile unlikely going anywhere
    - thinking about mobile devices and headsets for example
    - maybe the reverse needed to be considered
      - natural growth of the effort from a working group to a sig
      - working group has less effort to stand-up and can be upgraded later
  - on the authority question
    - need clear definition
    - areas of specific concern like xr or console have similar requirements
    - would want to avoid detrimental cross cutting decisions
  - discussed whether the mobile group would operate like a centre of excellence where they were reached out to for mobile topics
    - not the right model in this case
    - as there are problems that need to be actively worked on, e.g. the binary size issue
    - as well mobile group looking specifically for a place that standards can be maintained
  - on prioritization
    - noted that it is true that other sigs have some of the same priorities
    - but they are not at the same priority, e.g. sig-core has lots of priorities with binary size being only one of them
    - might want to fast track and bring visibility to different issues
    - not sure if a working group would bring the desired visibility
      - also noted that with the sig model visibility is not always as good as desired either
  - on working structure details
    - working group can have github group for better visibility
    - definite need to keep the communications level high between mobile effort and other sigs due to cross-cutting nature
    - e.g. when it comes to something like image formats do we have 4 tickets in 4 areas?
    - what about issue triage?
    - a working group hadn't been formed previously
    - a sig would be a significant amount of policy and structure more than a working group
    - a working group would also get a Discord channel if needed
    - what about PR's and if folks in the mobile group made changes in graphics, for example
      - sig-graphics should be included to review and approve
      - i.e. working groups work through sig's
        - if cross-cutting issues in an area, in case there are outlying immpacts
      - what about if we had a PR for battery power?
        - how would we tag a mobile member
    - can have github, discord, and mailing group
  - need to have the interested parties in the same place
    - multiple at O3DCon
  - initial interested parties focused on android at the moment
    - we have a platform/android label that can be used
    - also no objection to having a more general platform/mobile label 

- discussion outcome proposal summarized and agreed to as
  - start with a working group with a discord channel
  - mailing group with a mobile tag
  - central point of communications through discord and tag
  - set it up as a working group from an operations standpoint
  - they will work with sigs on the first two issues that will help define its starting point and growth
  - decided to move forward on this basis


### Emergent topics

#### Roadmap creation and maintenance

- currently do not have a roadmap for each one of the sigs
- desire to have an understanding for the sigs of what they might be working on in the next six months
  - homework item for sig representation
- feedback on the last release has been incredible
- things are now starting to work
  - a testament to the community efforts
  - now sigs can focus on what they, i.e. sig members, want to do
- there is currently a discussion thread that sigs should contribute to
- discussion ensued as to the formats to use for presenting a roadmap
  - list of tickets we want done that can feed into github feature boards?
    - e.g. godot uses this method to summarize tickets being worked on
  - higher level feature aspirations and areas being worked
    - e.g. unreal uses this format 
  - pros and cons of each discussed
    - general theme vs. specific items
    - ability to connect roadmap with the upcoming release
- discussion on the difference between what's for sure going to be in a release versus what there is community intent to work towards
  - different things
  - important to flag correctly
- with roadmap in place can poll community feedback on areas for priotiziation based on interest
  - having it in place and communicated viewed as important
- discussed that it's ok to state intent for something to make it into a release and then it not make it
  - unexpected things, technical and otherwise, happen
- even a short list is a good place to start to build out from
  - chairs need to meet with their sigs and bring it up
  - get something on paper so to speak
  - even if not complete
  - need a first draft, a spark, to work from
  - with a first draft in hand others in the community can assist
  
  

    






















 


