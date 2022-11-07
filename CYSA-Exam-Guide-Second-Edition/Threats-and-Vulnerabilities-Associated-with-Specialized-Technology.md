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

- 