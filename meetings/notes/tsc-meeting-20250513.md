# TSC Meeting - 5/13/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L. A.
* bluecat3183
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Matteo [Loharangrin]
* Michal Pelka [Robotec.AI]
* Nick_l
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Sid_MOudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - No announcements

### Discussion - Jan Hanca

https://github.com/o3de/sig-core/issues/44

* Last week I asked a question about the version for this week, and I promised to have a look into the existing docs.
* There is a RFC, written by Alex Peterson a long time ago (august 22 in sig core).  Its more about the implementation
  about the gems and engine.  Also a few paragraphs on the numbers and version of the engine gems and projects.
* From that perpsective, everything thats written there could stillb e implemented in practice.  I will giv eyou a link
  to the RFC in the chat.  The pipeline for the number is quite typical for all the software I know, so its described
  in such a way that if we create a stab out of dev, the stab takes the same version as the dev branch.  At the same
  time as we create the stab branch we should bump the minor version to make sure the dev branch is more modern and 
  ready for new updates than the stab branch, so that we only push fixes to the stab branch.  So we don't have to change
  the API and we don't have to bump the revision number anymore.
* I agree with this pipeline, and know it from different software, and what happened in the past (seperating the ver)
  is counter-intuitive, mainly becuase we have to go back with the engine deps in all of our gems.  We create gems
  in the development version and then after the release we have to change the version in all of our gems to work with
  the stabilization branch, so, as mentioned I will send you a link to this RFC, and I invite everyone to have a look
  at it.  Most of the RFC is the impl, but we could come back to the pipeline for the versioning numbers as well.
* Another thing we should keep in mind, this is an open question, when to bump version.  If its minor or major.
  HEre with the engine, the engine has its own version and gems have their own versioning scheme.  Changes of API in
  those gems.
* JOE: I think that if its a core gem that the engine won't run without, then the versioning should be tied to that.
* Jan: As proposed by nick, I can cut the important part from the RFC and prepare a RFC only for versioning.  
* JOE: I recommend getting everyone in the same space, getting opinions, etc.  For instance, who knows how this will
  affect atom or script canvas etc, so thats why I think a small WG for a temp time to just hash it out.  Versioning
  is extremely important, it took 6 months to get hte current versioning system approved.  I agree with everything
  you are trying to do (minimize dev and stab and releases) and also being extremely careful about how we bump versions
  and what we bump major and minor.  Historically: Bump minor when no breaking changes, point releases bump minors.
* Major is supposed to be when there's breaking API changes.  We haven't really bumped major versions in a while, so
  2.4 for a while, so we need to discuss that and get agreement on.  We should get input from all the stakeholders.
* We didn't bump ANY version on the dev version for quite a while.
* JOE: A feature author can go "oh, we detect there is a compatibility issue, we can write code to convert the current
  version 2.2 to 2.4, we can write code to convert over".
* JOE:  Thank you for pushing this along.
* JOE: A pillar of this effort is a section in this RFC that is impact to the user.
* Jan Hanca : We have a standard template for a RFC in our github.

### Discussion - Is it possible to request to push something to stabilization branch?
* O3DE-Extras, since we can now test everything against SDK, we found some problem in tests in o3de-extras, which
  we can solve now or for the point release, its not blocker or critical.
* Joe:  We have 3 weeks from today for the release.  If we follow our standard procedure, tuesday 20th is the code lock
  date again.  What will happen is, if you can get your stuff in (do put it on the exception board!)
* Joe: You can get it in, exception process must be followed.

### Discussion - Joe and Matteo - Sig release
* June 3rd is new release date
* Code lock, 2 weeks before the release is hard lock.
* Get any changes onto the exception board and get them in before the 20th.
* If its a minor, its likely no, there are a lot of users who do run the tests.
* The tests help protect us from our selves, so its important for them to be working.
* We have a new SIG-Chair for SIG-RElease, and so we are at the release meeting, they will attend, we can do formal
  introductions, etc.
* Now that we have a sig chair that frees me to focus on director stuff, foundation memberships, etc.  Running sig-release
  does not let me do this.  Having the chair for sig-release will allow me to free up to talk to companies, get them to
  help fund O3DE, etc.
* Thank you everyone, for hopping onto issues quickly and resolving them for the release, its very much appreciated. 
  Quality over date.  They will forget that we are 3 weeks late, they will not forgive a buggy or low quality release.
  We err on the side of quality over dates.
* Jan:  Sig-release meeting?  I see it in the calendar in 2 weeks.  
* Joe:  Today at 9:30 PST.  

### Discussion - Particle editor
* We're still working on getting particle engine/editor in.  I'd like the code to be public, so that people can maintain
  it and etc.  Its one of the disadvantage for o3de.

