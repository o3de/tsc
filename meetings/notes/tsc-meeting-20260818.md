# TSC Meeting - 8/18/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Amompharetus
* Arbiter
* Hellaenergy (Nick) [Red Hat]
* hex
* Jan Hanca [Robotec.ai]
* jayrulez
* JT[SCB_Network]
* Mike_C [Amazon]
* Nick_L
* Sergio Rojas
* Sid_Moudgil [Amzn]
* Steve P [Amazon]

### Announcement - Hellaenergy (Nick) [Red Hat]
* We put together the release schedule, its been posted on Sig-Release, and I'll post it here on the channel
* https://github.com/o3de/sig-release/issues/372

### Discussion - 3p package / O3DE Binaries - hellaenergy
* Introduce RPM into O3DE Binaries - point to instructions to point to copa repo
* Seems like it would be most financial practical way to distribute it right now.
* We'd have to be open about the fact that its still somewhat of an experimental build.
  I have a stabilization RPM out there, dev goes out weekly.
* JT [SCB_NETWORK] - also working with another linux distro (Alma Linux) to give it feedback.
* Open3d engine COPR from Hellaenergy is on the Alma Linux list already.  Really fast growing distro.

### Discussion - Arbiter - Sig-graphics RFC
* Moving AZSLC into the code base, looking at that would be useful.
* Sid:  Its probably okay, it was a different team, I'm not opposed, send me the PR, I'll find time
  and give an approval. Keep improvements separate from this effort.  Do integrating, then keep a 
  separate PR for improvement.
* Sounds like a good idea, because it was always a bit of effort to make changes.  If this is now
  part of repo, is there some document somewhere of how you want to push a change?

### Discussion - monorepo / RFCs for schema 2.0
* Discussion is ongoing, especially in light of the gists from @eric.

### Discussion - JT - Community Connect meeting.  
* Didn't record it (just a hangout and chitchat)
* We need to come up with a specific format, committing to october meeting
* The conversation was so outstanding, we could have made it a podcast!  
* We also had a few days before that we had a spontaneous chat, the most people in the community ever, 
  bigger than this chat we're having now.
* I also do an informal friday followup
* People chiming in with solutions (for when Nick_L is busy and can't chime in)
* People are getting to know the engine well (besides NickL) and helping out

### Discussion - Backports - Jan Hanca
* Is there a way to describe it ? https://github.com/o3de/sig-release/pull/356
* Maybe we need to update the readme.md to indicate the asynch nature.

### Discussion - JT - happy 5 yrs birthdays for open 3d engine
* Since the repo went public 5 years ago
* collecting info, got a skeleton of a slideshow, then highlight reel, then release in october to generate
  community outreach.  Just reminder, if you see me talking about it, if you have info from prior years, 
  hit me up, I'll point you to a thread, so we can collaborate.


