# TSC Meeting - 10/13/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* ChristianHinkle
* colinb[APMG]
* ElPicaronCL
* Hellaenergy (Nick)
* hex
* Jan Hanca [Robotec.ai]
* Nick_L
* RoddieKieley [Red Hat]
* phandradee
* Sadie (Chogan/Artist)
* Shauna [Genome Studio]
* Steve P [Amazon]
* u78PL

### Announcement - Hellaenergy (Nick) - SIG Release
* Splash Screen Submissions ending tomorrow, then Picking splash screen to include in 26.10
* In addition I've submitted review notes for each sig, please review.
* Release is still 28th.

### Discussion - Jan Hanca - TSC Message sent 
* I wanted to mention that there was always a problem with releases of o3de-extras.
* Every gem we release that was pulled by a project manger we upload to github release.
* So far it was always release 2.0
* Right now there are too many files in release 2.0, github does not allow this anymore
* We will not be able to make a nother release.  We are either required to make another placeholder, or do it the right way
* I decided to do the second way.  I changed the repo.json file and the PR is there so that all the past releases of all the old gems
  starting from 23.09 are uploaded to the correct releases.  Because every single gem while being released, it is zipped and the
  hash is being calculated to ensure we pull exactly the same code we are supposed to, I had to modify gem.json of every gem, because
  the path of the uploaded zip is in the gem.json file, so changing the place the data is stored required to recalculate the checksum
  and to recalculate the checksum I had to change it in gem.json.  I didn't change any of the 2.0 zip files, however, from now on
  I will ensure that the gems are uploaded where it should belong.  I did it for the past releases so everything is in order for
  the last 3 years.
* https://github.com/o3de/canonical.o3de.org/pull/41
* https://github.com/o3de/o3de-extras/pull/1104
* (colinb) we're trying to get all the verisoning worked out, for schema 2.0, for example, hash is inside the package, package contains the
  reference to the hash.  If we take the hashes out of that file, then we're kind of breaking the object.json into 2 pieces, and one
  part would be the pure object.  The way around it is we've been erasing the hashes out of it, and then you hash the object, and you
  should contain the hashes inside.
* (jan hanca) In gem.json we only keep the link to the object.  Not the hash.  We have just a link in the gem.json.
* (colinb) Distributability without authority (only hashing).  Once you have hashing and indexing.
* (colinb) Package manager - assumes the security risk of storing the official hash of the data.  The people who submit the packages
  compute their hashes.
* (colinb) confabulations that happneed during the repo.json, we tried to get it seperated into an advertisement, version of it.
  Repo.json is just an object that is like an open3d extras.
* (colinb) Curation is the other thing
* (colinb) Some countries have laws about that stuff, like we'd have to seperate it.
* (colinb) Discovery is important, some place where people can look and find these things.
* (colinb) What we COULD do, is have an extremely small curated list, which only has our objects in it.  A list of our own objects,
  just LF-Foundation objects.  Everything else goes into an uncurated list which is not officially "Sanctioned"
* (colinb) the point is just that the list exists somewhere and is not official but not automatically added.  You just get the list.
  You can add your links.
* JT: Peer review - popular place where other community members put their eyeballs on.
* crowdsource, vote up / vote down kind of stuff, community driven
* Community reporting - someone can flag it as a problem, bad objects go down, best objects go up
* AI could look at these things, not considered human curation (no laws around that).
* (jt) Local open-weight models narrowly scoped are really good and effective.
* Shauna: on the gem front, most of the stuff is already in place, kinks to iron out for 3rd party gem stuff, for the broader ecosystem
  management, but the basis is all there.
* Multiple repo.jsons is fairly striaghtforward/easy.  I've been struggling with standardizing on the data that is in the repo.json
  and finding a gold standard.
* (JT) Version number is all janky you see all the gems are janky
* (colinb) Most objects don't have version numbers at this point.
* Shauna - Data consistency standpoint / o3de extras json is all over the place, version stuff can be toplevel, some could be nested
  farther down in another object, etc.  Thats one thing I've liked about schema 2.0 plans.  To get it more standardized so that third
  parties can be more effective with that and all the json config files.
* (colinb) - related - I have not heard back from the 1 person who left a lot of feedback on the systme and its been like 2 months now
  maybe 3 months.  I'm going to move forward with the next iteration and I encourage anyone interested (opal, etc) to benefit from
  this feature to be more directly involved.   
* (Shauna) I put some feedback on your response gist.  we might want to figure out how to discuss / find the most recent version and
  path.
* (JT) I took a look at it for the first time, posted in discord, sent an email, I haven't posted yet on github, gist, etc.
  Discoverability was an issue.  I don't believe you are going to hear back from him.  I looked into it myself.
  I don't think he has any intention of comin back, its a one shot deal.  onee point is very strong - forest vs trees, its to borrow
  from UE5.  A lot of people went to UE5, gotten layed off.  copying or being inspired by some of their tech may be an attractor for
  prior devs of o3de and unreal engine.  It may impact engine devs.  Any good will gesture, if its close enough, they will form up
  around it and help move it along.   We really need to onboard more developers.   Lot of artists.
* (colin) The difference between mine and chris's approach was slight.  I'd like to hear someone argue for that side.  I'd love to
  hear someone argue from his side.  We've never chased Unreal's tail ever, and we shouldn't start chasing it.
* (jt) I did put the link to the architecture guild.  They are experts all over the place.
* (colin) One of the points of contention, is I've always advocated from the reorg of the objects in the engine, we came from cry
  and everything was in one place.  So we've resisted moving the objects out to be siblings instead of objects in the engine.
  This makes one of the main goals (Schema 2) possible, a monorepo that we all work on, and a consumption repo, that people would
  be using a day to day basis when downloading, small bite-size what I need and not what I don't need repos.  
* (colin) We have tools like git-repo-filter that can extract a folder from the repo, and that smaller object can link back to the main
  repo
* For chris's idea to work it would necessitate us keeping the gems under the engine objects, and making many more objects, and put
  them under a project object.  It would change the way we think about the engine, and I'm not so comfortable with that, it
  would be the "engine" and "the" project, instead of "a" project.  The idea is that you have a singular project and that project
  gets mutated into whatever you want by adding things to it.  I like the idea of the many differnet project objects, and the
  project says what engine it wants, and there's a solve (chris is against solving), so no workspace, ship the monorepo the
  format that is a solve, so you can build it without a solve.  But you could also still use a workspace out of those objects,
  its an accomidation that we necessarily shouldn't make.
* shauna - As painful as moving things around might be, people might be quiet about it becuase there's no alternative, or just
  to make the changes in house.  Genome has kept a number of chnages we've kept in house that we ahven't been able to get in upstream
  and OPAL is doing a lot of work to smooth out those pain points.  One of the issues WRT specifically file structure is the fact
  that there are gems nested within gems, and they are gems in gems and stuff like that.
* (colinb) I'm going to start executing on that in a branch in o3de.
* Shauna - I will repeat - for next time
  * Sig Graphics-Audio-Leadership needs shoring up
  * proposed Concerted stability pass for 27.10 release, and it was met with a lot of good results.  Would like to repeat it.
  
