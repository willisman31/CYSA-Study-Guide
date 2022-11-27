# Cyber Kill Chain

## Introduction

- developed by Lockheed Martin in 2011, the cyber kill chain is created to help blue teams understand the phases of an attack by an APT
- the phases are:
	1. Reconnaissance
	2. Weaponization
	3. Delivery
	4. Exploitation
	5. Installation
	6. Command and Control
	7. Actions on Objectives

## Reconnaissance

- collecting information about a target system
- OSINT and email harvesting are often key actions of this phase for attackers

## Weaponization

- creation or selection of weapons/exploits used in an attack
- malware = malicious software
- exploit = program to take advantage of a vulnerability
- payload = malware that runs on the defended system

## Delivery 

- how the malware/payload is transmitted to the attacked system
- common vectors include:
	- phishing
	- liberal distribution of infected USB drives
	- watering hole attacks

## Exploitation

- taking advantage of a vulnerability
- zero-day = vulnerability previously unknown to defenders
- lateral movement = change of attacked system to find a way to escalate privileges

## Installation

- create persistent backdoors
- common avenues include:
	- web shell on webservers
	- meterpreter
	- creation or modification of Windows services
	- Adding "run keys" to Windows registry or startup folder
- timestomping = modification of timestamps for actions performed on file to avoid detection

## Command and Control

- remote manipulation of target system
- also called C&C or C2 Beaconing; communication between C2 server and agent
- common channels are HTTP(S) and DNS through DNS tunneling
	- DNS tunneling = infected device makes constant requests to attacker-controlled DNS server

## Actions on Objectives (Exfiltration)

- may include some of the following activities:
	- credential harvesting
	- privilege escalation
	- internal recon
	- lateral movement
	- collection of sensitive data
	- deletion of backups/copies
	- overwrite/corrupt data

