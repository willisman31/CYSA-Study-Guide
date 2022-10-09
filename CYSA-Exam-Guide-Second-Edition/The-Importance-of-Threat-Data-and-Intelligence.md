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
