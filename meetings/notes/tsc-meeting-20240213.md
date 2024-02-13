# TSC Meeting - 2/13/2024

## Chair and Co-Chair
* nick_l
* Tobias Alexander Franke [Huawei]

## Attendees (By Discord name)
* nick_l
* colinb[apmg]
* Steve P [Amazon]
* Nicole Huesman [LF]
* Luis Sempe [Amazon]
* Sid_Moudgil [Amazon]
* null

## Agenda items

### Agenda Item (Ad-hoc) nick l next week out
* Nick L will be out next week.  Can anyone cover this meeting?
* colinb[APMG]

### Agenda Item (ad-hoc) - Colinb VIsion Pro - (Apple)
* Would need a large amount of work to get vision pro working via the XR gem
* Would be metal backend --> XR Gem --> Metal version of the XR gem.
* You'd have to also use the Platform Abstraction layer, as it counts as its own OS (Vision OS)
* Sid - there's a RFC for integrating the apple shader language directly into o3de, apple last year implemented their own compiler, but work needs to be done to integrate it into o3de and go directly from DXIL to apple shader.  At least 3 weeks of work, but once its there, thats step one for vision pro.  I'd imagine vision pro would have api and shaders and would likely complain with SPIRV-CROSS (just one maintainer)
* Sid - once that's done you'd have access to all the apple shaders like mesh shaders, all the special apple shader things.  You can write your mesh shader in HLSL and it outputs DXIL and apple compiler would take care of the rest.  The compiler lets you provide a binding schema.
* https://github.com/o3de/sig-graphics-audio/tree/main/rfcs/AppleShaderConverterIntegration

