# TSC Meeting - 5/13/2025

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* Andre L.A.
* Jan Hanca [Robotec.ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Luis
* Matteo [Loherangrin]
* Mike Chang [Amazon]
* Naomi Washington [LF]
* Mike S. [Carbonated]
* Nick_L
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Release is in 2 weeks!
* Use the exception board.

### Discussion - Joe:
* We have a new sig-release chair.  Onboarding, hoping they'd make it this morning.
* From Red Hat, w/ 20 years of open source experience.
* Name is: Hellaenergy (Nick) [Red Hat]

### discussion - Joe - Discord
* Discord has become extremely busy as of late!
* Lots of people creating PRs and contributing back.
* I am seeing certain SIGs struggle under the weight, especially sig-graphics-audio
* I would like to request that every sig have at least a second person that is reliable that can answer questions etc so we don't
  just rely on one.
* Sig-content Luis is the primary responder, Gaian helps out which is appreciated, there's a signal here that we need to take a look
  and make sure that Luis has help.  Its one of the larger sigs (it and sig-graphics) in terms of what they cover in the engine.
* 2 extremely well run is sig-platform and sig-simulation, their chairs are active, I see responses, several people, and that's
  the reason - I don't want people burning out because they're the sole end of the funnel.  Not worried about sig-simulation,
  lots of people involved, but I am concerned about sig-content and sig-graphics.
* Joe:  I know, nick, you are trying to cover as many bases as possible, but its insane for one person to cover millions of lines
  of code.  We're getting super busy, our download numbers, our discord activity, our github activity keeps growing, we are going
  to have to grow and become more organized in response.  I just don't want us to stall out because we are not set up to handle
  that kind of bandwidth.
* Nick:  How can we help sig-graphics/audio?
* Joe:  We need to identify in the community, ie, akio, etc, but identifying people who are willing to be active, having that conv
  and deputizing these people so they feel empowered and willing to speak up and represent sig-graphics, which is only the chair
  and co-chair can do.    One of the roles of chair/cochair is to manage people in their sigs and grow that.
* Sid:  I just want to add, in my current capcacity I am able to provide guidance, if I have to code, I get stuck.  I have to put
  aside, sync, compile, get running, spend time, etc.  I am most efficient in non-code guidance, looking at PRs, if I have to fix
  bugs, its a hard time commit.
* Sid:  Every time I have reached out for help, anton has provided guidance.
* Joe: Sig-graphics and sig-content are two extremely large sigs, one of the things I'd like you to work on 2025 is just the number
  of people you are comfortable with answering questions.  Sid you're going to go on vacation, I hope you do, we can't just rely 
  on one person for a sig like you are.  This is not calling out anyone for doing something wrong - this is just a heads up, 
  we need to fortify our posistions, we are going to keep growing.
* JT: I have a slack tour to onboard ASWF, as soon as I'm done with that one, I have scheduled to put one together for this
  discord server, I could get that done before the october release.  How to use it more effecitively, that might help.  One thing
  I did want to compliment - that tag team between sid and nick was awesome.
* Sid:  someone from huawei is joining the sig meetings, if someone from huawei is looking to take more of a role that would be great.
  His team only focuses on multi-gpu and cloud for example so thats the issue with huawei. 
* Joe: They do have another team I'm aware of that cares about other parts.  Naomi, next board meeting we can discuss this how
  companies can help keep up with that.  Mostly, I'm not going to call huawei but it would be cool if there were one or two people
  who could attend sig-graphics.
* Sid: I don't care about meeting, but take a look at the discord once a week and answer questions.
* JT: Tobias used to be active?
* Joe:  He moved teams and I think higher up on the rungs.

* JT: Speaking of chatgpt I'm seeing more code submissions that are actively chatgpt, coding for people they actually work under their
  own name and hire out the coder.  I found that very extensive in other projects.  We are going to get a lot of chatcgpt code
  submissions.  So call that out, there might be a bigger flood of PRs that are generated.
* Joe: I wouldn't say immediately dismiss AI code, but we have maintainers to make sure the quality of the code, however it is
  generated, remains consistent. 
* JT: The volume may just increase to the level where its very hard to manage.
* Joe: I'm seeing a bunch of people that might graduate to maintainers, in the next few months.  As long as we're active in not just
  maintaining prs, but growing our user base.
* Mike Change:  Some of the AR stuff is going on, we optimize for that, we will have more oppotunities that verify that it works.
* Joe: These are all great problems to have.  All foundations and open source projects want these problems becuase it means that
  the foundation is growing.  But I'm raising the flag to say sigs should think about how to keep up

### Discussion - Mike Chang [Amazon]
* There was some discussion on what to do with LFS, just to be clear, we do have free usage of github LFS, what may be the ultimate
  path here is coming up with a proposal for converting all of those assets to github LFS.  Then just kind of outlining the risks
  if we have any.  I don't see particular issues with it.  Where we are at the graciousness of github for this benefit, so, 
  its something we have to be considerate of.
* Joe:  Technically microsoft.  I owe you the contacts, I will get them to you.
* Joe:  If Github makes its LFS nonfree, it will put everyone, not just us.  We're paying for our LFS right now, so if they start
  charging it'd be more of a pricing thing.  I don't see it a big deal to move over.
* Joe:  Let's stage it, try test moving something thats small, move a test case over, then move over to larger and larger things.
* Joe:  The advantage of moving to github LFS is that then we are consistent inside the ecosystem.
* Joe:  I still need to get that graphic up.  I was able to build and test the new splash screen and it gave me so much issues.
* Mike: only maintainers can actually merge code into the primary branches.
* Joe:  Moving to github Actions was about cost.  
* Joe:  Moving to github LFS is about quality of life for contributors.

### Discussion - Mike Chang [Amazon]
* Status check: 15,000 hours of github actions time. Accounts for $1000 if we had payed for it.
* There has been slowdowns in the windows build me and nick have been looking at.  I've been trying various ways to get around
  it, it only seems to happen recently.  Interesting slowdowns have occurred.  I think I've figured out for the majority of the
  issues, thanks for nick going back and forth troubleshooting
* A lot of writes is going to the C:, including the temporary stuff, and we're migrating all of that temporary drive usage to
  the workspace drive which is a lot faster in comparison.  Overall we are looking at slowdowns over time but we are going
  to continue working on that.  I don't think we're ready to use it in the real branches yet but at least its a little better
  than currently, currently it fails over 6 hrs.
* Goal is later this year to make a GHA default for this.  We can always run the JEnkins AR.  There is a fallback strategy
  which I'm investigating that, we can utilitize other github action runners, etc.  There are some strategies we can do.

### Discussion - Matteo (release)
* Matteo - don't think 

### Discussion - Joe: fully offline installer.
* Get a GHI issue on the fresh / cdn issue, cause the CDN to refresh. As each version gets replaced, theres some amount of
  least-used caching and its not evicting the things it should.  Get a GHI on that.  Its not that important since its not
  the release builds work.
* We need to move the post-install stuff to the O3DE gui. Make the options appear for 3rd party, install, etc.  That change
  plus the reliability.  
* SHould we make the offline installer just the default, the whole thing?  
* I don't want to uninstall when you encounter an error.
* Is the installer under sig build?
* Yes
* After the release before the begining of june, lets talk about priority of this, etc. 
* GHAR is the highest priority but once we get thru that, we can thread between getting zip file, and installer simple
* Find someone who knowns / understands wix to make updates to the install.

