# The Importance of Threat Data and Intelligence

## Introduction

- threat data leads to threat intelligence when processed by quality analysts
  - threat intelligence = knowledge of malicious actors and their behaviors
  - cyber threat intelligence = *actionable knowledge and insight on adversaries and their malicious activities enabling defenders and their organizaitons to reduce harm through better security decision-making*

## Foundations of Intelligence 

| Discipline | Name | Description |
| ---------- | ---- | ----------- |
| SIGINT | Signals Intelligence | Intercepts of electronic communications |
| HUMINT | Human Intelligence | Intel gathered from all human sources |
| OSINT | Open Source Intelligence | Collection of publicly available information in any form |
| MASINT | Measurement and Signature Intelligence | Non-SIGINT data and imagery intel |
| GEOINT | Geospatial Intelligence | Imagery and geospatial data |
| All Source | All Source | All data available on a subject from all of the above disciplines |

## Intelligence Sources 

- the reality of the commercial space is that intelligence sources are limited (not so much in government)
- a combination of free and paid intelligences sources tends to be a winning combination in industry

### Open Source Intelligence

- OSINT must be free and legitimately acquired
- OSINT helps keep security professionals on the same page as industry trends
- used to discover threat indicators for specific actors
- used by pentesters for discovering potential attack vectors or weaknesses
- OSINT is helpful for malicious actors because it allows them gather intelligence without directly interacting with the target
  - passive reconnaissance = process of gather intelligence about an entity without interacting with it directly

#### Google

| Operator | Results | Example |
| -------- | ------- | ------- |
| site: | limited to specified domain | site:github.com |
| inurl: | specified contents must exist within url | inurl:/willisman31 |
| filetype: | results are only of the specified file type | filetype:pdf |
| intitle: | pages with the indicated text in their tile | intitle:Github |
| link: | results that contain a link to the indicated url | link:github.com/willisman31 |
| cache: | results contain only google's latest cached copies of results | cache:github.com/willisman31 |

- further google dorking operators can be found [here](https://hackr.io/blog/google-dorks-cheat-sheet)
- visiting the google results during recon will leave a trace of your presence
  - to avoid leaving a trace, use the Google-cached version

#### Internet Registries

- internet registries are needed in order to manage domains and IP addresses and prevent conflicts and overlaps

##### Regional Internet Registries

| Registry | Geographic Region |
| -------- | ----------------- |
| AFRINC | Africa and parts of the Indian Ocean |
| APNIC | Portions of Asia and Oceania |
| ARIN | Canada, US, parts of North American islands |
| LACNIC | Latin American, parts of North American islands |
| RIPE NCC | Europe, Middle East, Central Asia |

- Regional Internet Registries (RIRs) = corporations that control assignment of IPs; each has their own geographic region of responsibility as denoted above
- RIRs get their authority from the Internet Corporation for Assigned Names and Numbers (ICANN)

##### Domain Name System (DNS)

- DNS = mechanism for assigning domain names to servers
- translates (human-readable) domain names into server addresses
- gain information about live DNS data using the following tools:
  - nslookup
  - host
  - dig
- DNS harvesting = process of interrogating DNS servers to discover information about a network
- zone transfer = copying of DNS data across multiple DNS servers
  - zone transfers are a frequent point of exploitation because they are accepted by default
  - managed by access control lists (ACLs)
  - can be initiated by another DNS server or from a client
- domain registration requires that the registrant provide details about themself (can be individual or organization)
  - details include the following:
    - name
    - phone number
    - email contact
    - DNS information
    - mailing address
  - these details can be harvested using a tool called WHOIS and are public by default
    - some registrars (companies/agents who indirectly lease domains from ICANN) provide private registration so that registrant details point to the registrar rather than the end client

#### Job Sites

- job site members provide lots of private information freely
- harvesting of this information is typically trivial
  - leads to easy phishing campaigns
- companies also make themselves vulnerable by using job sites- if a company is looking for a SME or admin with a particular experience, it's likely that the company uses those technologies

#### Social Media

- Reddit and Twitter in particular are useful sources of rapidly updated information about live events
- social media sites are also useful mediums for gathering target and attacker information based on their public personas
- social engineering also makes use of social media both as a platform for attack and for targetting specific individuals using personal information mined off these sites

### Proprietary/Closed Source Intelligence

- never rely on a single source in intel gathering
  - reduces confirmation bias
  - helps ensure more successful campaigns as intel is more accurate
- OSINT is often best used to corroborate closed source data

#### Internal Network

- analysis of internal network activity helps establish a baseline for activity
- internal network data can come from the following sources:
  - DNS
  - VPNs
  - firewalls
  - authentication logs

#### Classified Data

- make sure that your closed source data is being protected before, during, and after you're done analyzing it
- classified data in particular requires additional protections beyond the scope of this section

#### Traffic Light Protocol

- Traffic Light Protocol (TLP) = color coded designations for information sharing
  - created by UK National Infrastructure Security Coordination Center (NISCC)
  - Not a control scheme, just a guideline

| Color | Usage | Sharing |
| ----- | ----- | ------- |
| Red - not for disclosure; for participant use only | use only when information cannot be acted upon by 3rd parties | not for disclosure beyond initial exchange |
| Amber - limited disclosure within participant org | requires support in order to be acted upon | to be shared only within participant org |
| Green - limited disclosure within community | useful for spreading awareness within community | share with peers and partner orgs, not with general public |
| White - unlimited disclosure | little or no risk of damage from release | distributable without restriction |

## Characteristics of Intelligence Source Data

- no such thing as comprehensive intelligence source- multiple sources must always be used to supplement and check each other
- prioritize data that can be used to produce *actionable*, *timely*, *consistent* results
  - good intel has 3 elements:
    1. timeliness
    2. relevance
    3. accuracy
  - noise generation and intel failure is inversely proportional to those 3 elements
- all commercial intelligence sources are too generic to be used alone

### Timeliness

- intelligence that is delivered too late is not actionable

### Relevancy

- prepare threat intel for the appropriate audience
  - provide details that are most actionable to the parties who will receive the intel

### Accuracy

- obviously anything you're presenting as truth should be maximally accurate
  - this means keeping assumptions to an absolute minimum if not eliminating them entirely

## Confidence Levels

- intelligence providers use 3 levels of analytic confidence
- these levels acknowledge incomplete or fragmented information
- these are human judgements, not objective quantitative measurements

| Level | Description |
| ----- | ----------- |
| High | based on high quality info; still possibly incorrect |
| Moderate | credible source and plausible; not good enough for high confidence |
| Low | too fragmented or incomplete as basis of solid analytic inferences; may be concerns about source(s) |

## Indicator Management 

- indicator = observable artifact on a network
  - include both data and context

### Indicator Lifecycle

- vet the indicator -> decide if indicator is valid
  - research origin, determine usefulness and reliability
- sharing threat data can help industry security operations

## Structured Threat Information Expression

- Structured Threat Information Expression (STIX) = MITRE-led effort to communicate threat data in common language
- STIX 2.0 framework has 12 SDOs (STIX Domain Objects) and 2 SROs (STIX Relationship Objects)
  - under framework, analysts show relationships between SDOs using SROs
  - visually representable with JSON
    - simple structure of data storage allows easy integration into automations

### SDOs

#### Attack Pattern

- attack patterns are a part of an attacker's TTPs (tactics, techniques, and procedures)
  - a combination of actions, not just a single event
- useful for describing types of attacks and *how* they are executed

#### Campaign

- collection of behaviors against a type of target over a set period of time
- campaign = attacks over a finite period that share the same attacker, victim (or victims), and type of attack

#### Course of Action

- preventative measures or reactions addressing an attack
- includes both technical and policy implementations

#### Identity

- representation of individuals, organizations, groups
  - may be entity specific (a person or organization name) or industry- or sector-wide
- the targets

#### Indicator

- observable data used to detect suspicious activity in an environment (network, system, device, etc.)
- must be accompanied by context in order to be useful

#### Intrusion Set

- compilation of a single entity's behaviors/TTPs/properties
- focus on resources and patterns of behavior rather than identity of the attacker
- different from campaigns because they are not bound by a set timeframe

#### Malware

- malicious software 
- type of TTP

#### Observed Data

- any observable artifacts derived from a system or network
- this is not quite information- it is raw data
  - information falls short of intelligence

#### Report

- finished intelligence product detailing aspect(s) of a security event
- may reference other SDOs
  - ties in relevant details to explain what happened

#### Threat Actor

- individuals/groups behind malicious activities
- sophistication, PII, motivations can all be tied into this object
  - understanding goals of a threat actor can help predict their movements

#### Tool

- software used in a campaign
- tools are NOT malware; may include common software development utilities or systems administration mechanisms
- can be more difficult to protect against because legitimate users may also use the utility and commercial protection mechanisms may not recognize it as a threat

#### Vulnerability

- software mistake
  - exploited by attacker for unauthorized access
- different from malware; may be targetted by malware

### SROs

#### Relationship

- connection between SDOs
  - explains how they interact
- below is an EXAMPLE of some common relationships

| Source SDO | Relationship SRO | Target SDO |
| ---------- | ---------------- | ---------- |
| campaign | attributed to | threat actor |
| malware | targets | identity |
| attack pattern | uses | malware |
| course of action | mitigates | vulnerability |
| indicator | indicates | tool |

#### Sighting

- provides information about an SDO
- heavy focus on quantitative details: 
  - last occurrence
  - first occurence
  - frequency
  - number of occurences
  - where were the occurrences
- next step up from observed data

### Trusted Automated Exchange of Indicator Information (TAXII)

- defines how threat data are shared between partners
- supports STIX data with API design
- 3 models for sharing:
  1. hub and spoke -> end users share data with hub by pulling and/or pushing to it
  2. source/subscriber -> subscribers pull down data from source- data flows outward only
  3. peer-to-peer -> peers share with each other in network
- 2 services:
  1. collections = interface for SDO storage
  2. channels = pathways for clients to publish data to other clients

### OpenIOC

- framework created by Mandiant (or FireEye- who knows anymore?) to organize attacker TTP info and other IOCs (Indicators of Compromise)
- machine-readable format for easy sharing and automation
- 3 main components:
  1. IOC metadata = indexing and reference info about IOC; includes author name, IOC name, description
  2. reference = describe how IOC fits into an environment and sharing guidelines
  3. description = everything else; the "meat" of the indicator

## Threat Classification

- incident = any activity that results in some form of harm to the system or increases likelihood of breach of confidentiality
- identifying incidents starts with establishing a baseline of normal system activity
- make an incident response plan

### Known Threats vs. Unknown Threats

- AV software, IPSs, IDSs, etc. use 2 mechanisms for detecting malicious activity
  1. signature-based = using historical data collected on known threats
  2. heuristic analysis = observe behavior as it happns and determine from there if the activity is malicious
    - leverage sandbox environments for testing executables and suspicious files
- absence of evidence != evidence of absence
  - just because there is no malicious activity detected does not mean that there is none
  - reduce assumptions to improve accuracy
    - one option is to treat everything as untrusted

#### Zero Day

- zero day vulnerability = software flaw unknown to the developer
- zero day exploit = code written to take advantage of zero day vulnerability

##### The Emergence of the Exploit Marketplace

- recent increase in zero day exploits
- due to their value, zero day exploits are sold in black markets to criminal groups that can profit from leveraging them
  - bug bounty programs are the other side of the same coin- software development companies pay distributed markets for first crack at their own zero days so they can be resolved before criminal exploitation

##### Preparation

- no single solution can protect anyone or anything completely
  - layer defenses and prevent single points of failure
- even with an incident response plan, organizations should have proactive operations to deal with security threats
  - info sources on software bugs:
    - SANS Internet Storm Center
    - CERT Coordination Center at Carnegie Mellon

#### Advanced Persistent Threat (APT)

- APT = stealthy continuous, usually coordinated, hacking effort
  - usually orchestrated by a government or organization with extensive resources
- goal is to maintain long term access to target systems while evading detection

##### Advanced

- well-equiped, well-trained, well-funded; APTs coordinate many sources of information to gather intelligence on a target

##### Persistent

- individual operators have a good understanding of their role in a campaign or hacking effort and can pinpoint weak spots through long-term engagement

##### Threat

- APT campaigns serve a larger purpose than a single cyber event in a bubble- there is a broader goal in mind and an attack represents just one step in achieving that goal
- because APTs are by definition advanced, successful organizations will very often share information about them so that they can be combatted on a bigger scale

## Threat Actors

- threat actors are a diverse bunch in terms of sophistication, resources, and intent among other things

### Nation-State Threat Actors

- these are the most sophisticated threats because of the resources, manpower, training, and support that can be provided to offensive programs
- with huge budgets, they can buy or develop their own zero days with great frequency
- may involve private businesses as contractors
- may incorporate false flags into their campaigns to avoid be identified by defenders
- simple intelligence operations for one nation may appear to another as a threat actor

### Hactivists

- attackers with a specific cause or purpose they are supporting outside of the government space
- typically reliant on large participation in order to be effective
- little (if any) emphasis on stealth or monetary incentives
- commonly attack availability of a system

### Organized Crime

- driven by monetary incentives
  - selling intellectual property
  - ransoming assets
  - stealing compute for crypto-mining
- generally low-risk operations with high return on investment
- growth of cryptocurrencies have allowed money to be moved more easily

### Insider Threat Actors

- threat actors that work from within an organization (pretty self-explanatory)
- traditional security perimeters are ineffective
- solutions to combat them must be multi-dimensional and layered

#### Intentional

- organization members with privileged access of some sort who wish to use their access for money or revenge
- combat with role based access control
  - monitor anomalous network activity
  - remove employee access upon termination

#### Unintentional

- human error or negligence can make people unwitting threat actors
- mistakes happen, good controls can limit the damage done

## Intelligence Cycle

- 5-or 6-step method for converting raw data into actionable intelligence
- cycle is continuous and can progress without total completion of the previous step

### Requirements

- question identification, prioritization, and refinement
- planning and direction as needed

### Collection

- data is collected to fill gaps in intelligence
- setting up data sources inside and outside of the system 

### Analysis

- making sense of collected data
  - utilize automation, trained professionals, or other means of data processing
- output of this phase is actionable intelligence

### Dissemination

- distributing of requested intelligence
- requesters can then utilize the processed intelligence as demanded by their organizational goals

### Feedback

- each phase includes a refinement; feedback phase is a dedicated part of the cycle when the team can reformulate their processes to improve
- self-appraisal as well as appraisal by client (whomever requested the intelligence)

## Commodity Malware

- pervasive malware made available for sale to other threat actors
- horizontal integration is about as common in organized crime as it is in modern business- just because a group can build malware doesn't also mean that they're optimized to profit from its delivery

### Malware-as-a-Service

- malware built to order
  - may include customer support, regular updates, bug fixes (Windows = malware /s)
  - often cloud-hosted to offer better service to buyers

## Information Sharing and Analysis Communities

- different industries have dedicated security-specialized communities for sharing information
- ISAC = information sharing and analysis community
- some examples are included below:

| Industry | Name |
| ----------- | ---- |
| Automotive | Auto-ISAC |
| Aviation | A-ISAC |
| Communications | NCC |
| Electricity | E-ISAC |
| Elections Infrastructure | EI-ISAC |
| Financial Services | FS-ISAC |
| Health | H-ISAC |
| Information Technology | IT-ISAC |
| MultiState | MS-ISAC |

- ISAOs (Information Sharing and Analysis Organizations) = public organizations for sharing security information not specific to a given industry