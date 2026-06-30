# TSC Meeting - 6/30/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Asgin (Chogan)
* ChristianHinkle
* Gaian [Genome Studios]
* JT [SCB_GameDesign]
* Kyler
* Nick_L
* Reece H. [DrogonMar]
* Shauna [Genome Studios]

### Announcements - JT
* I do searches every so often to see what kinda traction we're getting
* A few new blogs have picked it up, we're getting more traction to expand the custom articles
  that people are blogging about game engines and tech.
* Particle system helped with that bump.

### Discussion - JT - JT Taking over the moderation of the reddit channel
* I've been hanging out there and monitoring the bridge channel in discord.
* For a couple weeks we had good traffic.  Letting everyone know that I'm working
  with a tight policy, since LF isn't handling this and is passing it to the community.
* I assume LF will keep the master keys to the discord and Joe has the priveleges required and
  has escalated me to admin for the channel.
* Within the next 2 weeks depending on how busy it is.
* Hopefully it will build up with the particle system and getting things outside the discord, in our github, etc

### Discussion - Gaian [Genome Studios] - We're working on a private project (engine reg)
* We're in the final (95% mark) and we're just having an unbelievable times with one of the most fundamental
  features, which relates to engine registration.  Basically, we have a very technical sound piece of tech
  that Shauna has been overseeing and with full confidence I've been exhausting every avenue to work around
  this, and the registration process for engines, is so non-granular, that more times than not in anyones
  circumstances, it overrides previous engines, loses tracks of engines, when you start to have many concurrent
  ones.  Once again, brought up schema 2.0 would very much alleviate these things.  
* We can get a much more granualar information from engine reg to make sure that the engine is registered.
* Its now costing us delay time and in fact preventing Shauna from doing the game dev time while we compensate
  for what is not working.  I feel its only going to grow in annoyance for ourselves and others and it might
  be time to start setting off on Schema 2.0 somehow and some way.
* Shauna - One piece that would make the largest piece of difference, its the engine name.  Right now
  every release version has the same engine version "o3de-sdk" or "o3de" if its the source.  There is no
  disambiguation, and the registration script treats itself as the source of truth, its what gets put into
  the registry.  Unless its been changed since I last looked at it, the registration fails silently if that
  name collides with anything that already exists.
* Another problem is that the projects reference the engine.  
* Gaian - when you build the project with an engine, the customized data on the project is project.json
  but the moment it builds with the engine, it goes into the baked user file, and creates a second project.json
  and the only thing that stores is the local path to the engine.  It then goes to that path, and then goes
  "Hey is that name to the engine?"  And then collides again when the names are the same and the most problematic
  is at two instances of source engine, and I'm about to get the third, they are called "O3de" alone.  
* The manifest takes the names and the paths with them, and then it completely ignores it all, pull up the path
  on the baked user project.json and finds out theres a name there.  The engine isn't the engine this was built
  with if the name mismatches.
* Shauna [Genome Studios] - If we want to pilot schema 2.0, let's use repo.json and use that to pilot it.
  If there's any place where introducing a formalized schema it would be the repo.json.
* Shauna - Related to the names, there's also a version.
* There's 4 versions.  (Use only one)
* (Insert the discussion on repos.json)
* Currently, repo.json and individual engine/gem/project/template jsons are wildly different.

Notes about above plan
TSC Discussion today suggested the following steps (In no particular order)

* Combine duplicates of EngineFinder.cmake into a separate template and make the project-creator script
  instantiate that into each project.
* Eliminate strict engine matching in EngineFinder.cmake, when the user has specified an engine explicitly
  such as via user/project.json or the module path.
* Register engines into the engine-by-folder list even if their names collide.  Continue registering them
  in the engine-by-name list for backward compat
* Modify EngineFinder.cmake to use the engine-by-folder list, and read engine.json instead of the by name
  list.
* For discussion with sig-release and etc:  Just call it o3de or o3de-sdk regardless of source or sdk.

