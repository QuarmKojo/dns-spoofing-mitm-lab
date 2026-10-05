# DNS Spoofing / Man-in-the-Middle Lab

Controlled virtual lab simulating **DNS spoofing** and **Man-in-the-Middle (MITM)** attacks, then evaluating defenses. Team project (Kojo Quarm, Tiffany Cooke, Martin Lawrence) from the Columbia University Cybersecurity Boot Camp.

> **Educational use only.** All activity was performed on isolated virtual machines I own. Do not run these techniques against networks or systems without explicit authorization.

## Environment
- Attacker: Kali Linux
- Victim: Ubuntu
- Tools: Ettercap, Apache2

## Demonstration steps
1. Enable IP forwarding on the attacker machine
2. Edit/configure the Ettercap DNS file
3. Host a fake webpage on Kali (Apache2)
4. Launch the attack with Ettercap
5. Victim visits the spoofed website

## Mitigations evaluated
| Layer | Controls |
|---|---|
| DNS server | DNSSEC (`dig +dnssec <domain>`), randomized source ports and transaction IDs, response rate limiting (RRL) |
| Network / system | IP source filtering and anti-spoofing rules, firewalls, regular patching |
| Monitoring / IR | DNS query logging and monitoring, sinkholing, regular security audits |
| User | Phishing and spoofing awareness, antivirus and browser protections |

## Documentation
- Slides: [`docs/DNS_Spoofing_Presentation.pptx`](docs/DNS_Spoofing_Presentation.pptx)

## References
- Ally Petitt, "Practical Demonstration: DNS Spoofing + Home Lab" (Medium)
- Akamai, "Weaponizing DHCP DNS Spoofing: A Hands-On Guide"
- Splunk, [Man-in-the-Middle attacks](https://www.splunk.com/en_us/blog/learn/man-in-the-middle-attacks.html)

## Skills demonstrated
Virtual lab design, network traffic analysis, ARP/DNS attack techniques, defensive control evaluation.
