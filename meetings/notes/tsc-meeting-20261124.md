# TSC Meeting - 11/24/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* Colinb[APMG]
* Iris *Cofree-Road)
* Astin
* Gaian[Genome Studios]
* Hellaenergy (Nick) [Red Hat]
* Jan Hanca [Robotec.ai]
* jayrulez
* JT [SCB_Network]
* Sadie (Cogan)

* Nick_L
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* u78pl (Jakub Cywka)

## Announcements

### Announcement - Release - Hellaenergy (Nick) [Red Hat]
* We had a successful release on 20th November, 26.10
* Things are going smooth so far.  We had a not-negative review from GamesFromScratch.  Any feedback around that would be great.
* We will be having a retrospective.  Today a half hour after this meeting, in #sig-release
* Thank you to everyone who contributed, and those who stepped up when I couldn't be there.  Just goes to show to have not a single point of failure
* We are looking for a sig-cochair
* Colinb: We have a gpu crash

### Announcement - Colinb - WG AI met for first meeting
* Iris is the new WG AI Chair
* Colinb is the co-chair.
* We have documentation from Shauna.
* The WG-AI repo has been created and we have started filling it in.  There is a lot of interesting stuff in there from the AI Proposal, I'll drop a link to the repo:
* https://github.com/o3de/wg-ai
* Next meeting is on monday 10am PST recurring (1900 CET).
* The meeting is open to everyone now.  Leadership has merge privleges for the repo, and we are deciding who is responsible for what.  anyone is able to participate, submit prs, etc.
* Pilot projects
* different ways AI can help us.  Perhaps in O3DE one day.
* Policy decisions.
* Running test repos vs AI.  Seeing if it can classify bugs, tag things, priortize things.
* Many different aspects we can deal with.  Decision is by community, the chairs, and co-chairs are there to take documents and etc, and don't decide what happens.

### Announcment
* I've posted a link for the release on linkedin/X/etc.

## Follow up check-ins

### Follow up - JT - Gaps
* Its going well
* We are figuring in how whats a gap.
* Papercuts, gaps, or feature extension.
* #sig-all has a topic link (thread) 
* #tac/tsc - decide on what is there.
* We'll more it to a discussion on github, that way we can get input from github.
* Learning how to evaluate these gaps is a valuable skillset.  That way we can act on them a lot quicker.
* Nick_L:  When do you expect to have some initial artifacts?
* JT: Thanksgiving and holidays are a bit of a blessing and curse, but I have a goal to have it this week.

### Follow up - ColinB WG for Schema 2.0
* colinb: Moving forward.
* colinb: I have an item in the official topics for the meetings so I'll defer to that.

### JT:  note - sig-all agenda item in the TSC repo

## Discussion Topics

### Discussion - Arbiter - Physx5 update
* If anyone wants to look at the new physics
  version, its ready to test.
* PhysX cloth has been updated to use the new omniverse
  or physx core APIs.  It would be good to just use physx
  gem handle that in the future since its mostly been integrated into the physx core now, instead of being a separate thing.
* You can pull the build artifacts from linux / windows its a bit tricky because its not in the CDN.  It has to yank them from the github workflows instead.

### Discussion - Arbiter - NVCLOTH
* I made significant changes to simplify the repo
  and update the cmake
* We had a bunch of lumberyard PRs that are applied on
  top of NVCLOTH.  
* Could we fork it into O3DE and have our own maintained fork.

### Discussion - ISPC TexComp
* Intel has abandoned and archived the repo.
* There are some improvements that can be made, like
  leveraging modern kernels AVX5 etc.
* That was another one I was wondering if we could fork.  I have perf enhancements, things we can fork.  The license is permissive enough.
* Arbiter:  I've tested others, like compressinator, and its significantly slower.
* JT: There are also other communities discussing compression.  If we look at this particularly we should look at it in general for texture compression.  
* Arbiter: we use "Oodle" (because its amazing) but thats very much a licensed product.  I'm looking at it as how can we improve the open source.

### Discussion - OpenXR / XR gem
* Is that something we can bring back into the main
  repo?  We've been doing testing with steam frame.
* colinb: Half the point when I created the XR gems, that was one of the first things we put into O3DE Extras.  It was to put it in there as part of proving the gem system.  there's no reason it could not be in the core repo.  It doesn't have to be in a different repo.  One advantage was that we could work on it faster.  It didn't have to be slowed down by the AR stuff we were doing.  I'm sure the guys in robotec.ai appreciate that they ahve a lot more control over the extras repo.  Its intentionally slower to develop in the core repo, the idea was that core repo was the more hardened repo and it should have more scrutiny and move slower.  This was the thinking of the time was that we needed to do most of our dev in o3de-extras where it could move faster, then vote on whether we wanted the object in the main repo.  If people find that an object (including XR) would be better of in the main repo, its very doable, we could push it right over, thats what it was made for.
* arbiter:  It feels a little slower to work in extras, we worked in Jenkins AR system to pull in all canonical repos and did its AR passes.

### Discussion - AI issues pull requests (Jan Hanca)
* Its about the time the workgroup is here.  I was not able to attend with the group due to the time.
* Recently there was a pull request, it was basically AI generated and the pull request itself was AI Generated.  I have nothing against it, but the code was okay, I made a comment and the code was reviewed by a human.  And I got a response to the comment, also written by AI.  No human involvement at all.  From my point of view, that was too much, after all we are a community.  I'm not going to interfere with the workgroup on AI.  I think it was a value to repos to added key piece of template to our pull request templates to issue templates to say how much of the work was AI generated and how much was human generated.  I'm involved in a few open source projects.  Just having to say "its all AI generated" stops people from posting a lot of AI slop.
* JT:  This is happening on docs too.
* colinb[APMG]: That might have been me, (ARGUS) that did that.  Part of talking about it in the working group.  It was probably me that did that, I have no problem being called out.
* Gaian : GUI Flattening work is very relevant to this
* https://discord.com/channels/805939474655346758/1571993816691642522 (GUI Flattening - Bench and Review)

### Discussion - Workgroup - Schema 2.0
* I updated the Lyshine branch.
* I would like the TSC start the clock on schema 2.0 workgroup.
* We can change the name like O3DE NEXT or O3DE TWO or whatever.
* Start the clock today.
* If we don't have at least 3 people we will extend for another week.
* JT: I think its bad optics on holiday week due to everyone being gone.  Why did you start it on a holday week when everyones gone?
* colinb[APMG] - I have no issue starting it now and beginning 3 weeks.
* Shauna - a lot of stakeholders (international) are not dealing with a holiday this week.  When you start taking on a global scale, there is a holiday every week.  People observing are going to have to understand that and we're not doing this maliciously and its not the only week where its open.
* JT: Its not necessarily the volume, its how you are treating critical people.

## Next meeting topics
* Discussion topic - Documenting Code
* Discussion topic - Coding Standards
* Lyshine Branch
* Translation branch

