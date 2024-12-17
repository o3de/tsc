# TSC Meeting - 12/17/2024

## Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* colinb[APMG]
* Guillaume [Cloud Imperium]
* Guthrie [Amazon]
* Jan Hanca [Robotec.Ai]
* Joe Bryant [O3DF]
* JT [SCB_GameDesign]
* Michal Pelka [Robotec.Ai]
* Moldawsky
* Naomi washington
* Nick_L
* Reece H.  [DrogonMar]
* RoddieKieley [Red Hat]
* Shauna [Genome Studios]
* Sid_Moudgil [Amzn]
* RoddieKieLey [Red Hat]
* Steve P [Amazon]

## Meeting Notes

### Announcement - Joe Bryant - Cancelling next 2 TSC meetings
* Next 2 meetings are Cancelled - 24th and 31st.

### Discussion - Nick_L - Reverb
* https://github.com/o3de/startergame-assets/tree/main
* Sid is working with Huawei on making change to the viewsrg/scenesrg optional or do it automatically (regarding scenesrg)
* Sid (Regarding the helper rendering) There should b a ring buffer for them, we should triple buffer for it, we should not make the allocations, so all the aux-geom debug, debug lines, debug shapes related should be a ring buffer and fast, should be pretty optimized.  If I had to take a guess, it'd be on the CPU side.
* NickL: We will profile it.
* Sid: (Regarding Shader tutorials) Shaders - lighting values, material information, that stuff is complicated and gets involved with material and pipeline system.
* Sid: Shaders - lots of them outside of that, here's a shader that does a blur , downsample, upsample, etc.
* Sid: I can look up a couple material related videos, in terms of god rays and stuff, it depends on how they might want to implement the feature, it depends on whether they want to do it as forward pass, or transparent pass - are they creating a material, custom material type, is it using the material canvas, is it generated, thru the node graph, etc.
* Sid: They could use atom sample viewer test bed / experimentation bed to build a quick pipeline, really quick one shader, add that shader to it.
* Sid: https://github.com/o3de/o3de-atom-sampleviewer
* Sid: There's a bunch of samples in the Atom Sample viewer, there are a bunch of features that are very small - like load a json and there's your pipeline and there's it.  Maybe the mesh sample is an easy one.  What that sample does is in the imgui you can click the mesh and click what materil it runs, and that would be for a material.  All the RPI samples, they are all really simple samples.
* JT [SCB_GameDesign] - I'll bump this up in the documentation schedule.
* (Multiplayer) - Client / Server sync between client/server on same machine.
* JT [SCB_GameDesign] - May be some sort of security workaround.

Below are the raw meeting notes from the Meeting with Reverb (from yesterday)

```
Meeting notes from meeting with Reverb
Monday 12/16/2024 - 8am PST

* So far, a year-old project, to be released on Steam, date TBD.
* Why O3DE?
  - Anatoliy went from Cryengine -> unreal engine -> lumberyard .2 version -> o3de
  - GTX 1060
* UI Toolkit: 
  - Lyshine extended?  Its LyShine for the UI
  - (Anatoliy) creted a modular UI - custom LyShine UI.
  - UI is modularly changed in game to show what is around - for example, pieces of the ui appear if there is items on the ground
* Project Language:
  -  entire project is No LUA - only C++!
  - 40,000 lines of C++ code at the moment in the project.
* Editor stability.  
  - (G) When you encounter a crash do you report it? 
  - (M) Its not crashing, its just closing.  Its many objects that can close its.
  - Crash on startup at random - see stack traces

  - (Anatoliy) I'd like to create shaders - please a simple example of a volumetric or surface shader without using other libraries -
 show how to create a simple material in o3de documentations, we have this, but in documentation we have informations and cool and useful 
 but no we havent' had a simple finished shader.  Its a very big and cool shader, but its difficult to understand.  If O3DE would have a simple
 surface, simple volumetric shader example, it would be cool.  Default shader is very difficult to understand hwo to create a custom shader.
  - We need volumetric lighting effects (lighting, fog, god-rays)
  - But we'd need some simple examples of how to add a volumetric, surface, etc.

  - (ISSUE) Render Helper FPS is super slow.  Like 5fps down from 60fps.

  - (ISSUE) Monolithic PAK files reading is very slow.  The game opens okay, but if you open ui canvas, it sometimes 20 seconds while it loadss
  - This happens only in PAK mode on PC.  Reading PAK file is very slow.  
  - Game tries to load a UI CAnvas, but any file from pak file, on PC it was very fast, milliseconds... on another, its 20 seconds+ while it loads.
  - It keeps showing it in readfile.
  - (SID) Shader variants can be created - 24.09 does not have the feature to do it automatically.  
  - (SID) Under the hood everything is using the most expensive shader, but you can build variants that are more optimized.
  - (Joe) If you're not planning to ship until next year, you could probably wait for the next release and use shader constants.
  - (SID) If you are not shipping on console you can use function constants / specialization constants.
  - Joe:  I would like a priority list.
  - Joe:  For the bugs that are mentioned, in what order would you like to have them resolved, whats the most important?

  - (Anatoliy) - Big problem in multiplayer - after I build mp sample or our game, when you start dedicated server and start them both from one pc
  - The client will not be synchronized with server. 
  - Joe:  we'll have to get SIG-network as well.
  
```

* Nick L to create issues?

* Issue:  Crash in mesh - SIG-Graphics -  Nick L to create issue and drop call stacks.
* Issue:  Slow helpers - SIG-Content - Nick L to create issue and do initial profile.
* Issue:  Duplication Issue - SIG-Content - Nick L to create issue and do initial profile.

* Issue:  shader tutorial / helper - Nick L to recommend they go to Atom sample Viewer 
  - Joe: The issue is our documentation doesn't point out the process of how to learn more about shaders, what is the process?
  - Joe: Documentation path or issue?
  - Joe:  Shauna ? You and Sid should talk about making it easier to find.
  - JT:  I'm working on it.  Shauna and Sid.  Its one of the things I'm helping out.
  - SIG-Docs can own this and take care of it how they see fit.

* Issue:  Pak File Slowdown
  - We need more info.  Joe?
  - Create Issue - and take down the information from there - contact info must be there too.
  - Moldawsky - create the issue (SIG-Core chair and find out what the next steps are.)

* Issue:  Network issue?
  - We need more info.  JT?
  - Client/Server - JT will work with whoever else.
  - Automatically be Gene - Sig/Network.


