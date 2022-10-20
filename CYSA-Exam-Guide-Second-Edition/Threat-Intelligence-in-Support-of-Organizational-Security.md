# Threat Intelligence in Support of Organizational Security

## Intro

- alert fatigue = too many false alarms, leading to decrease in responsiveness from incident responders
  - adding more layers of threat intelligence increases context for events and decreases false alarms

## Levels of Intelligence

- security efforts should impair the ability of threat actors to attack or damage the organization
- threat intelligence needs to work to anticipate attacker actions
  - various levels of threat intelligence must exist so as to inform different levels of an organziation's hierarchy to take appropriate actions

| Level | Description |
| ----- | ----------- |
| Strategic | Highest level of intelligence; used to inform organization leaders of key concerns; not overtly technical |
| Operational | Who/when/what are we defending and for how long?  What should be done to achieve strategic goals and what resources do we need? |
| Tactical | Precisely what are the defenders doing in response to actions by attackers; highly actionable level of intel |

## Attack Frameworks 

- frameworks add structure to thought processes and aid in understanding concepts, timelines, and motivations of attackers
  - better understanding of attackers means it is easier for defenders to stop them

### MITRE ATT&CK

- MITRE = federally-funded research organization with cybersecurity specialty
  - created the following systems and frameworks:
    - Cyber Observable eXpression (CybOX)
    - Common Vulnerabilities and Exposures (CVE)
    - Trusted Automated Exchange of Intelligence Information (TAXII)
    - Structured Threat Information Expression (STIX)
- ATT&CK = Adversarial Tactics, Techniques, and Common Knowledge 
  - has 3 flavors:
    1. Enterprise ATT&CK = *SEE BELOW*
    2. PRE-ATT&CK = TTPs used by attackers before launching an attack
    3. Mobile ATT&CK = TTPs used by attackers to get at mobile platforms

#### Enterprise ATT&CK

- most widely used and relevant ATT&CK model
- 12 categories:
  1. Initial Access - how they get into your network/system
  2. Execution - run malicious code on your system
  3. Persistence - maintain presence on your system
  4. Privilege Escalation - gain positions of higher privilege
  5. Defense Evasion - maneuvers used to avoid detection
  6. Credential Access - gathering of names, passwords, tokens
  7. Discovery - increase understanding of network/system
  8. Lateral Movement - pivot and gain access to other systems on network/subsystems
  9. Collection - capture of artifacts
  10. Command and Control - taking control of your system by attackers
  11. Exfiltration - getting your data our of your system by attackers
  12. Impact - what is done by attackers to destroy or damage your system/network
- common language is important for communicating across teams
- hundreds of techniques across categories 
- [MITRE ATT&CK Navigator](https://mitre.github.io/attack-navigator/enterprise/)
  - allows tracking of techniques, tactics, and offenders who commonly utilize them

### The Diamond Model of Intrusion Analysis

- developed by Sergio Caltagirone, Andrew Pendergast, and Christopher Betz to emphasize relationships and characteristics between the following:
  1. Adversary
  2. Capability
  3. Victim
  4. Infrastructure
- model is dynamic, adjusts with adversary actions
- model integrates with 7 axioms which capture the nature of all threats (supposedly):

| Axiom | Conclusion |
| ----- | ---------- |
| Every intrusion is trying to produce a result which furthers the goals of the adversary | Every incident involves the 4 components of the diamond model and can be mapped against them |
| There are adversaries that want to compromise systems for their own benefit | Threat actors are always there; if we know what they want, we can better protect our systems |
| Every system has vulnerabilities and exposures | No technology is purely safe with no exceptions |
| All malicious activity has at least 2 ordered aspects required for successful exploitation | Dependencies must be fulfilled in successful attacks; break the chain, break the attack |
| External resources are needed in every successful attack | Preventing attackers from effectively leveraging these resources will limit the effectiveness of their attempts |
| There is always some kind of prior relationship between victim and attacker | Attacks are becoming more and more difficult to execute, so attackers will only dedicate much time to victims that hold significance to them |
| There is a subset of attackers capable of and motivated in sustaining prolonged malicious efforts against any given victim; these are *persistent adversaries* | Determining which operations require long-term access in order to succeed can help defenders combat them |

### Kill Chain

- phased model which organizes enemy activities in a military operations
- common example is F2T2EA (Find, Fix, Track, Target, Engage, Assess), born from Air Force need for responsive, agile framework to improve air strike response times
- cyber kill chains exist as well to break down attack stages to help defenders pinpoint where in an attack they can develop the most effective countermeasures

#### Lockheed Martin Cyber Kill Chain

- developed in 2011 as whitepaper by security team members
- consists of 7 steps:
  1. Reconnaissance
  2. Weaponization
  3. Delivery
  4. Exploitation
  5. Installation
  6. Command and Control (C2)
  7. Actions on Objectives
