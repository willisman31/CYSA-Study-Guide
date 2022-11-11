# Threats and Vulnerabilities Associated with Specialized Technology

- attackers look for the easiest path to exploitation
- once all the easy ways in are remediated, the attackers are likely to move on to an easier target (unless there's something very special about your assets)
- common flaws found way too frequently:
    - missing patches/updates
    - misconfigured firewall rules
    - weak passwords

## Access Points

- WAPs are some of the most commonly vulnerable network components
- BYOD policies pose a challenge for security teams
- WEP is insecure and should NEVER be used in a secure network
- rogue WAPs can be connected to a network unless additional protections are implemented
- IEEE 802.1X standard should be implemented
    - client authentication required
    - granular access controls
    - minimum patch/update requirements for connected clients

## Virtual Private Networks

- VPNs connect devices that are on different networks as though they are on the same
- VPN connections are made using several special protocols:
    - Internet Protocol Security (IPSec)
    - Layer 2 Tunneling Protocol (L2TP)
    - Transport Layer Security (TLS)
    - Datagram Transport Layer Security (DTLS) (Cisco devices)
- VPNs can expose corporate networks to dangers by allowing untrusted, unpatched, and infected devices to connect from anywhere
    - we can keep out untrusted connections by requiring a preinstalled certificate on clients
    - we can keep out unpatched connections by implementing Network Access Control to actively check update status of clients before connecting

## Mobile Devices

- given their uniquely privileged access to private data, they are a lucrative target for attackers
- mobile devices are much more susceptible to physical theft than other computing mediums
    - "physical access is total access" - it's much harder to protect data when it's literally in the hands of attackers
- three categories of mobile vulnerabilities:

### Network Vulnerabilities

- 2 network entries:
    - attacks from poorly configured/built mobile networks
    - attacks on the mobile device's mobile interface
- when the network infrastructure itself is exploited, everyone who uses it is vulnerable
    - this is especially problematic when threat actors have government-level control over these networks
- attacks on mobile interfaces are rare, but high impact events

### Device Vulnerabilities

- vulnerabilities to a physical device can be absolutely devastating because the only remediation is to get a new device
    - a really cool example of this is the rowhammer attack
        - this attack is based on how dynamic RAM (DRAM) is accessed in modern computers where a small electrical signal changes leaks to nearby cells in memory whenever a certain cell is accessed.  In theory, this can be leveraged into privilege escalation by creating a large enough electrical charge to change specific memory addresses.  Realistically, it's basically impossible in any practical setting, but it does show that virtually all hardware is susceptible to attack

### Operating System Vulnerabilities 

- developers aim to limit time between patch release and installation; attackers want the reverse so they maximize the time that an exploit is viable
    - window of vulnerability = time between vulnerability discovery and patch installation
- Android devices tend to have larger windows of vulnerability because of the need to coordinate across multiple vendors
    - iOS doesn't have this problem because of its centralization

### App Vulnerabilities

- 