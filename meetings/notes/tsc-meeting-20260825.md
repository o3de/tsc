# TSC Meeting - 8/25/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* Cheddarspice [iamjbq]
* ChristianHinkle
* colinb[APMG]
* hellaenergy (Nick) [Red Hat]
* hex
* JT [SCB_Network]
* Nick_L
* RoddieKieley [Red Hat]
* Sergio Rojas
* Steve P [Amazon]
* Yaakuro

### Announcement - JT
* Started a few threads in the server to improve engagement, projects that can be community-organized projects
* Dry-run on a hackathon, but I'm doing it in conjunction with other platforms, and will be including the open 3d community
  in the dry run and walkthrough.
* Got some traction in real life here in So Cal, we'll see what happens online
* Along with that, OS Hackathon (which will become an event of its own, we have an initiative thats a lot bigger than o3de)
* I have a lot of work to do with docs - github workflow so we can collaborate more with community, on how we can coordinate that better.
* Gaian and I have been doing this on and off for a while.

### Discussion - Nick_L mimalloc instead of HPHA
* Location: https://github.com/microsoft/mimalloc
* License:  MIT
* Docs: https://microsoft.github.io/mimalloc/
* We should be able to toggle it off by compile option
* Other allocators are available too.
* What about iOS and Android support
* mimalloc could always build with debug or HPHA too!
* unreal has Binned 1-4 - console specially have memory characteristics and alignment things, and more importantly, it really likes
  arena/pool allocation.  Unreal and o3de struggle with lots of heap allocations, and mimalloc is really good for that in the editor,
  and placement news, but its not super great on consoles.


