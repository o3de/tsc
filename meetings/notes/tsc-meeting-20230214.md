# TSC Meeting - 2/21/2023

## UX SIG delivers their report

# Chair and Co-Chair
* nick_l[amazon] 
* Tobias Alexander Franke [Huawei]

## Attendees
* Nick_L [Amazon]
* Tobias Alexander Franke [Huawei]
* geds-dm [Amazon]
* RoddieKieley [Red Hat]
* Bhanuja [Amazon]
* Seapip [Amazon]
* Yuyi [Amazon]
* Joshua Rainbolt [Amazon]
* Royal OBrein [LF]
* JT [SCB_GameDesign]
* colinb [APMG]
* kberg [Amazon]

## Agenda Items
* https://github.com/o3de/tsc/issues/68 
The UX team would like to review the year-end 2022 RTE survey results with the group and then discuss next steps.
https://docs.google.com/document/d/1A8nm1tHmbPLN4F6Wu0WtHv-YxgrLwIoxxwNkhT6b3O4/edit


###  Topic:  Royal updates
* A better bot that allows better recordings.  the recordings will be able to transcribe them to text
  to review them.
* A bot that can show each day's discussion as an email digest
* Documentation: Collaborative - hedge doc that allows people to collaborate in markdown.  if its useful I can put that up.
* Other elements being worked on like being able to make a tag in discord which creates a discussion in groups or in github.

###  Yuyi - Topic:  The UX team reviews the year-end 2022 RTE survey results
(NOTE from Nick,  this was a guided walk through of the document at the following URL.  These notes are largely redundant vs the content in the document below.  For brevity of notes here, I'll try to capture the things that were mentioned or discussed but NOT on the below doc.  Unless otherwise specified, comments are by Yuyi.)
* https://docs.google.com/document/d/1A8nm1tHmbPLN4F6Wu0WtHv-YxgrLwIoxxwNkhT6b3O4/edit
* Contains a REV-THE-ENGINE Results document
* Review the result from the REV-THE-ENGINE results document
* As SIG-UI/UX we can suggest and help drive improvement but lack the ability to implement them across the engine.
* (Doc is reviewed linearly here, section by section)
* Average score is average but able to be improved.
* Blue lines is June result, Red is December result.
* packaging and deployment needs improvement and has lower scores
* Just going thru this quickly because you can go thru the report yourself. We will also be posting it on the blog.
* In addition to the above questions, Rate your Agreement to the following Aspects of O3DE
  * Results for Ease of Resolving Issues is really low!  Error messages are not helpful.  content helping the customer is not well connected with use cases.
  * We want to call this out for the team to consider.
* O3DE is below the software industry benchmark
* At the end of the survey we asked open ended questions to provide feedback  We have collected the feedback to present here.
* (Joshua Rainbolt) NPS score is evaluated against other types of industries as well.  This is a particular one, (software), but I think its good to note that this MPS score evaluates against all software out there, ie, Word, etc, is a benchmark of "happy factor" for NPS score.
* NPS stands for Net Promoter Score.  it is an industry standard with one question ("How likely are you to recommend this product to friends and colleagues?").  Behind this question is a very well calculated formula to figure out how likely the user is going to use this service and be an advocate.  There is an industry standard to define where is the bar.  Theres a 0 to 10 you can choose how likely to recommend the software to other people.  If you choose a 7-10, you are a strong advocate.  the rest is neutral to negative.  For example, a 2 would be a detractor, they might recommend AGAINST it.
* (JT:) I use this a lot and put it on slides for CEOs in the Fortune industry.  The most important thing is that your score improves over time, nto necessarily where it lands initially.  The key metric that is looked at.
* NPS Score is a reference and consider how much we can improve in our product.  I wouldn't say this is bad, its a signal for us to continue improving. There's a lot of things we can do, like getting better customer or user experience in O3DE.
* (Document reading continues to the feedback section)
* We categorized general feedback into different groups - error handling, documentation, etc.
* Large amount of feedback about error messages.  Lots of suggestions from the customers that we collected.
* We also prepared a dashboard with issues on the github.
* End of presentation.  
* The impetus is to build more and more features that compare to other engines, but fundamentally there are usability problems we really need to solve to get users onboard easy and build basic functionality easily.

Dashboard links: 
* https://github.com/orgs/o3de/projects/42 - Rev The Engine (RTE) Dashboard
* https://github.com/o3de/o3de/projects/15 - Walk The Engine (WTE) Dashboard

### Topic:  open discussion
* Joshua Rainbolt:  PArt of the reason the TSC needs to be involved in this is we need to be able to start assigning things to individual sigs and resolve them as problems.  How we take it on and when we take it on is going to need TSCs help to assign and divide this work.
* Royal:  Q for UX team.  did you include the complexity of material for these workflows?  something that is a simple square that you connect to a square that you put into another square, vs something that you import from blender with tons of shapes?
* Yuyi:  Survey result came from everyone in the community.  We asked them what they feel so far in terms of UX.
* Yuyi:  In addition to that, we did a Walk The Engine where a customer is invited in to perform some task, and we asked users to bring their assets with lots of complexity in the model.  We interviewed a game developer from New World for example, they brought their building hut in, with lots of really complicated process and gave us feedback for the survey.
* Royal:  Normally people would be using blender, maya, 3ds, I gave Sandeep one recently that was built in blender and it brought it to its knees.  it wasn't that the geom was complex, but the sheer volume of little things like LODs that were in the way and cluttered.  I asked about complexity - if I throw something like a chair, its easy, if I do something greater, its a very different experience.
* Yuyi: I think those are considered in the survey results.  They may be using this feature in a simpler use case, or complex and struggling.  for those feedback we should record those in the rev-the-engine dashboard so that the UX team can look at them.
* JT: (explains that in things like blender, users who regularly do a workflow find workarounds reasonably quickly and find a way to do efficient work around the deficiencies and problems).
* Royal:  O3de brought in like, 100 sub-meshes, were put together in the prefab.  There was a ton of extra things that really made it difficult
* Yuyi: Think of this as all the customer feedback.  The feedback here indicates that the customer already managed to actually get into the engine and enjoyed their experience.  We didn't record users who dropped out and could not make it into O3DE in the first place.
* Royal:  Why not?  why not note that they fell out at a specific point.
* Yuyi: We didn't record this in the survey - we invite 75 customers to run the WTE.  None of them are O3DE users - from game dev/user panel, all have used Unreal or Unity.  They went thru the process and the onboarding experience were not good and most of them fell out and didn't participate.  There is that.  There is hard to continue with the rest of the workflow because of the onboarding experience.
* royal: can we do the basic stuff first, like the stuff you'd be in unity or unreal, and the steps to open those objects and get them running?  But if we have people dropping out before they can do that the rest is irrelevant.
* Joshua:  that's a good point, royal.  There is a workflow 1 that focuses on onboarding.  We can always walk you through the footage of that.  This is more holistic end-to-end.
* Royal:  Before worrying about a passing grade of everything else, get an A on your basics.  Don't boil the ocean.
* Yuyi: I would say, if we look at this 9 workflows, onboarding and game-play would be the most important ones.   If we want to extend to animation systems and world building, thats four of them.  This includes how to bring the assets in, how to manipulate it, set it up as a basic way.
* Royal:  bringing assets in, there's a misconception that theres no assets but you can bring in anything from Unreal, Unity, packages in.  and some of the different nuances, blender, unreal, etc.  You can use many objects from the unreal store.
* JT : Keep in mind in the game industry, 2 users.  one is tinkering on their own they drop out cuz they have a certain on the time.  Someone could be payed to do an engine evaluation - the tinker is more likely to bounce.  Someone who's been tasked with engine eval will spend more time.  Put aside 1-2 weeks full time to eval.  Keep that in mind.
* Royal:  Lots of people in the industry will play with the engine then later shoot it down before it even gets a fair eval.
* JT: Happened to blender.   When the major smoke plugin studio suddenly raised the maya price to really expensive. 
* Yuyi: We need a working group!  We need a collaboration between sigs.  Its hard for us to approach to each sig, it would be great to have a group of people to improve the UX.  
* Royal:  Working group and TSC meeting.  you can get a bunch of people from the community that would contribute.  You can build a single repo that they can simply have a project they are working on thats all about elevating this.  A working group exists for as long as is necessary.  You can fire the working group up, you can keep it going and then shut it down when its done.  You put a charter together that want to do this.  Propose it to the TSC, get feedback we will ratify it.
* JT: We use them extensively in ASWF.  I can help walk you through it.
* Colinb:  the output of your working group should be the creation of issues.
* NickL/Royal:  working groups can also work on code.
* Colinb:  Sigs or working group doing this?
* Royal/Yuyi:  The working group.
* JT:  once it kicks off like it does in ASWF they become very popular.  Bunch of people get in and see results it works out well.


### Call for ADHOC agenda items
* Royal: opening a thing about tagging and flagging on groups.io.  the means for us to expand our communications model.  Ltos of discussions in discord gets lost, this can with one command push to the groups and keep its history.
