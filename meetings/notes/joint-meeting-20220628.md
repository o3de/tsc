# Joint TSC : SIG Meeting 2022-06-28

## Attendees

- Karl Berg
- Nick Lawson
- Roddie Kieley
- Royal O'Brien
- Jeremy Ong
- Tobias Alexander Franke


## [Agenda](https://github.com/o3de/tsc/issues/37)

- SIGs should update their respective repository top-level READMEs to include information about:
  - SIG function/objective and role
  - Participation links (calendar, Discord, list)
  - Meeting information and invitation to participate
  - Can draw content inspiration from the community [CONTRIBUTING.md](https://github.com/o3de/community/blob/main/CONTRIBUTING.md) page
  - *Action*: Jeremy to email SIG list regarding the request
- New [`notable` label](https://github.com/o3de/o3de/labels/notable)
  - Should be used to designate PRs and issues as being relevant for marketing and outreach initiatives
  - Hints that a PR may be linked to a blog post, announcement, or other form of amplification
  - *Action*: Jeremy to email SIG list regarding label

## Emergent Discussion

- @galibzon (SIG/graphics-audio) chair mentioned that a Mitsuba exporter was approved by the SIG for ground truth comparisons
  - Tobias mentioned that a colleague (Huawei) has been working on this, to be shared/released at a later date, with one additional goal being a graphics research accelerant.
  - Royal expressed interest in extending the exporter to other engines/renderers
  - Currently developed solution is strictly export-only instead of a runtime or editor integration (license issues for runtime, editor may be possible)
  - *Action*: Royal to work on exploring options for editor integration, with license restrictions similar to Qt
- O3DECon PSA
  - CFP (Call for proposals) for talks and presentations are open, people are encouraged to submit early or reach out for content feedback/suggestions to Royal
  - *Action*: Jeremy to include the O3DECon PSA in the email


## Detailed discussion log

-- more descriptive README.md
There's a discoverability problem, at the top level readme should detail what the repo is
requested that we add a bit of the 

how to access the discord
what the sig does
- see the template doc from Finchy

- royal
-- so in original charter had  the info
-- so should be able to grab the info there and put it in the README

- jeremy
-- will e-mail chairs

- royal
-- overall community group sigs
-- community under contributing

-- see the notable label



- emergent discussion

- galibzon
-- did due diligence into what a good ground of truth provider for the renderer
-- some ppl started to file bugs some renderer images don't look identical to the same scene in unreal or other engines
-- philosophical discussion about quality via comparison to other engines
-- need engine agnostic "specification"
-- gpu path tracker mitsuba2
-- potentially generate xml scene to provide ground truth provider as what the scene should look like


tobias
- a colleague has been working on this
- now have comparison renderings mitsuba vs o3de in pixel perfect match in a specific scene
- and can no id things that need to be able to fix
- code not yet available
- have to talk to the colleague about the PR

royal
- if looking to create a ground truth
- would be good to work with mitsuba 2
- could approach unreal and unity

tobias
- unity one was the one that I wrote
- will dig up the link

royal
- could be a good opportunity as another 3D project

jeremy
- what we're talking about is not something that does a reference ray trace at run-time
- export and import into mitsuba 2 at the moment
-- data focused
- if we wanted to move forward we'd need some sort of license worked out for O3DE

royal
- can work on the license pieces

jeremy
- clear delination with the binary

royal
- goal would be to match mitsuba's reference
- would be a great project as all renderes would like to standardize

tobias
- 1 thing to get out is for academic research
- e.g. real time algorithm for paper
- how to match the cameras or resolve sub-pixel issues


jeremy
- research angle is a great one
- what if someone wants to add additional caps
-- off line baking
-- vs. ddgi or something like this


royal
- get a thread going
- will dig around about something viable
- can work on at the tac level

jeremy
- other topics
- Roddie Kieley from Red Hat was previously voted Co-Chair



royal
- quick pitch
- O3DCon coming up
- if folks have things they want to write
- drafts/cfps
- sooner makes it better to establish how to do a bunch of pieces
- keep that kin mind

tobias
- had some talks internally
- 3 topics from there
- hotels in austin are not so good

jeremy
- will make a mention of the O3DECon in e-mail as well