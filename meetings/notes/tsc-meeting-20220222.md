# TSC Meeting - 2022-02-22

## TSC Attendees

* Karl Berg
* Phil Keslin
* Jeremy Ong
* Nicholas Lawson
* Tobias Alexander Franke

## Request to remove the bug label

- Question around if the bug label was created intentionally (it is redundant with kind/bug)
- Believe it's a default label we can remove

## Request to create a task template

- Question for future: Should GitHub administration and operations be delegated or should these issues remain a direct responsibility of the TSC?
- Recommendation is that future RFC for the task template be written
- Question regarding people opening tasks that they don't intend to complete. In general this is fine because sometimes, you need to socialize an issue before working on to get buy-in before working on it
- Request for a doc describing the difference between a task and a feature, as well as clarity on the goals around filing a task/feature in light of the above point

Followup: PR to community repo to describe the task template in more detail, will be socialized on mailing list and discord later

## [Sig-simulation](https://github.com/o3de/tsc/issues/14#issuecomment-1042808611)

- There was some push back regarding the operational overhead of sig-simulation
- Feedback that if there were people willing to chair and co-chair the sig, there isn't a bandwidth problem and all the previous discussion points about the potential value sig-simulation would bring stands
- greedv and tomhh informally offered willingness to oversee sig-simulation

Followup: finalized charter for TSC to vote on

## [Deprecation strategy followup](https://github.com/o3de/tsc/issues/14#issuecomment-1042809484)

Not discussed due to time constraints

## [Sig-security](https://github.com/o3de/tsc/issues/14#issuecomment-1047150899)

- Open question about SIR (Security Incident Response) team membership, and TSC's involvement
- One suggestion was to initially add SIR nomination to current sig chairs
- Possibility of TSC management still stands

Followup: will need additional discussion

## External gems, and commercial gems

- Suggested that they be removed from the primary O3DE repo
- Commercial partners likely want to develop the gem on a development cadence not coupled with the primary repository and O3DE governance
- Development on the main repository is unlikely to scale if all middleware or commercial partners include their code/gems
- Partner promotion is outside the purview of the TSC and can be accomplished through other mechanisms, in collaboration between the docs team and the LF

Followup: Nicholas Lawson to draft an RFC for discussion