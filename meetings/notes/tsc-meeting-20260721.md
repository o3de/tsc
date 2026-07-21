# TSC Meeting - 7/21/2026

## Chair and Co-Chair
* Nick_L
* (Co-Chair pending)

## Attendees (By Discord name)
* Arbiter
* Hellaenergy (Nick) [Red Hat]
* hex
* Jan Hanca [Robotec.ai]
* Mike_C [Amazon]
* Nick_L
* Reece H. [DrogonMar]
* Shauna [Genome Studios]
* Steve P [Amazon]

### Announcement - Mike_C [Amazon]
* I'm currently in the midst of moving the LFS infrastructure other than AWS.
* I had some dicussions with the LF, and we've managed to secure a cloudflare account to handle LFS and LFS deployment as well as binaries
* The net benefit is that cloudFlare does not charge for egress.
* Do we want to continue deploying some of the things, 3p, fetchcontent updates, help lessen the load on the CDNs.  And I'll have an update soon.
* What that means is we'll continue using AWS, for some time. I've discussed continuing funding for our AWS accounts, and discussed whats our plan
  to more or less separate that infra from AWS completely.
* Github is not necessarily reliable at the moment, so using the 'releases' page is questionable.  Maybe as a backup.

### Announcement - Mike_C [Amazon]
* Part 2: In regards to a discussion with Joe, regarding canary jobs.
* The canaries have been running, but pinning versions of the compiler to is problematic.
* For example, we pin the version of the vs compilers to the wrong one, we'll fix that
* The part that we might discuss is, what do we do, when we encounter a failure in the canary jobs.
* (Nick): What about just some status badges?  We can start from there.

### Discussion 
* Style Sheets optimization by nick
* Discussion in the discord - thread about Qt6 - but the summary is that style sheets are very slow to evaluate, and happen whenever the styles
  on a widget change.  This occurs when you reparent a widget to nullptr, or move it between places in the hierarchy, such as `setParent(nullptr)`
  to put it in a widget pool and hten subsequently take it out of that pool.


