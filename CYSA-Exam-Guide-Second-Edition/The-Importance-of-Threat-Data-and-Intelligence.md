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

- 