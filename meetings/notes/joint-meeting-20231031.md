# Joint TSC : SIG Meeting 10/31/2023

# Chair and Co-Chair
* Nick_L
* Tobias Alexander Franke [Huawei]

## Attendees (by discord name)
* geds-dm [Amazon]
* Nana Yellen
* JT [SCB_GameDesign]
* Naomiwash
* SanB [Amazon]
* null
* Sid_Moudgil [Amzn]
* Kepler
* Nicole Huesman [LF]
* Alex P [Amazon]

## Overall outline
This meeting has been recorded.  
link: https://drive.google.com/file/d/1LnAy_fuB7W0a2OD9gE14MT8HRhjoUBPn/view

### Agenda Topics

Github meeting issue: https://github.com/o3de/tsc/issues/101

#### SIG Updates
##### Sig-Core updates (geds-dm [Amazon])
Posted updates in the o3de/tsc repo at https://github.com/o3de/tsc/issues/101#issuecomment-1787391369
Added new RFC to discuss topics to improve first time Asset Processor experience.

##### Sig-Graphics-Audio Updates (Sid_Moudgil [Amzn])
Progress is being made with improving the Shader Management Console application.  
Improvements to memory and GPU usage on the mobile platforms.  
Meta is currently working on VR pipeline. Suggested that work should go into the AtomSampleViewer project.  
Huawei is working on GPU and ray tracing for Skin Meshes. Ray tracing passes happens after skinning.

#### Sig-Release Updates (Naomiwash)
The 2310 Point Release has been moved to December.  
Next O3DE Connect November 8th at 11AM PST (1PM CST).  
Meeting link: https://discord.com/channels/805939474655346758/900458901655420938/1168930748900843611.  
Looking for volunteer for show and tell. Lloyd from Carbonated presented tutorial in the prevous meeting.

Looking into Spin-Off meeting with Joe Bryant around the Point Pelease.  
Also looking to know if the No-Code project is ready to be added to the Point Release.  

#### Questions
- SanB: How is the Mac Editor doing?
Sid_Moudgil: It is experimental. There are some crashes, but no one has been using it in depth.
Can reach out to Carbonated to discuss what is broken and working on MacOS and Metal.
Asset Processing is slow on MacOS

Topic: Best Practice Guidances for improving workflow
* Sid_Moudgil: SIG-Graphics-Audto has guidance around authoring Shaders: https://github.com/o3de/o3de/wiki/%5BAtom%5D-Shader-Management-Console-(SMC)
* null: Wanted to known if RFC has been brought around products declaring Source Dependencies when it comes to Asset Processing. Brought the possibility of using being able to cook product assets on demand instead of cooking ALL assets from every available Scan Folder on startup on the Asset Processor to improve iteration. Having source dependencies would allow products to know what it needs to process in order to cook assets on demand.
* null: There is no proper dependency on cooked asset to source asset


