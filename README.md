




# EHC-Resources
EHC is the Ethical Hacking Club at Auburn University. The plan is to use this as a starting point and to be a hub of resources, from beginner-level to advanced-level.

### Contents
- [Digital Forensics](#digital-forensics)
- [Open-Source Intelligence (OSINT)](#osint)

# Digital Forensics
What is Digital Forensics?
- Digital Forensics is the process of collecting, preserving, analyzing, and presenting digital evidence for legal use.
- This [video](https://youtu.be/UtDWApdO8Zk?si=uw4qxHQ0Q3dXB-Oq) will help explain the basic concepts and legal implications of digital forensics.

Steganography
- [Steganography](https://youtu.be/I9WwX3EHdyY?si=nOG3SNtRa6Fj78C5) is the process of hiding information inside images, videos, text, and other digital mediums.
- [StegOnline](https://georgeom.net/StegOnline/upload) is a simple tool beginners can use to un-steg an image.
- There are also several command-line tools for deciphering steg. This [blog](https://0xrick.github.io/lists/stego/#tools) describes use cases for each.
- [Aperi'Solve](https://www.aperisolve.com) is another resource similar to StegOnline that can be used to perform layer analysis on many different file types to check for hidden messages.

Network Forensics
- A big part of Digital Forensics is analyzing the traversal of data over a network.
- An Intrusion Detection System (IDS) provides automated alerts for suspicious traffic over monitored segments, decreasing the time between an incident and incident response.
- Packet Captures, or pcaps for short, are considered the gold standard of network evidence.
- Unlike summarized data from logs or Netflows, pcaps capture headers and payloads allowing forensics specialists to reconstruct entire conversations, application-layer interactions and verify what data was affected.
- [Wireshark](https://www.wireshark.org/) is the leading application for packet capture analysis; this should be your go-to.
- [Tcpdump](https://www.tcpdump.org/) offers many command-line alternatives for network analysis, especially with pcap.
- For more information about Network Forensics, visit [this](https://www.forensicfocus.com/guides/network-forensics-a-short-guide-to-digital-evidence-recovery-from-computer-networks/) site which elaborates further on the topic.


[def]: #digital-forensics

# OSINT
What is OSINT?
- OSINT, or Open-Source Intelligence, is the process of collecting and analyzing publicly available data to produce actionable intelligence.
- Some forms of OSINT you may already be aware of is the data linked to your google account and social media sites, but this is just the tip of the iceburg in terms of public data.

How important is it to protect my data?
- There's a litenany of reasons you should protect your data from public viewing.
- Allowing random people on the internet access to your personal information makes you a target for identity theft, cyberstalking, online scams, and more.
- If you are having trouble understanding how your personal data can lead to victimization, this article on [data brokers](https://www.aura.com/learn/how-to-remove-yourself-from-data-broker-sites) shows wwhat these adversaries can do with your data.

How do I protect my data?
- Fortunately, there are many resources available to someone who wants to protect their privacy online.
- VPNs such as NordVPN, Surfshark, or (the free option) Proton VPN encrypt your data and mask your IP address from potential bad actors.
- Anti-malware software such as [Malwarebytes](https://www.malwarebytes.com/) (which is free) protects you from threats lurking in emails, texts and other messsaging formats.
- Password managers such as [Bitwarden](https://bitwarden.com/) can be used to vault your passwords, ensuring you and only you have access to that information.
- Ad blockers such as [uBlock Origin](https://ublockorigin.com/) (make sure it is uBlock Origin and not the defunct uBlock) protect you from malicious sites and advertisements.
- [AbuseIPDB](https://www.abuseipdb.com/) is a project dedicated to helping combat the spread of hackers, spammers, and abusive activity on the internet. You can report an IP address associated with malicious activity, or check to see if an IP address has been reported.
- You can also attempt to manually opt-out of data brockerage sites, as described in the [article](https://www.aura.com/learn/how-to-remove-yourself-from-data-broker-sites) from the previus section.

Tools:
- [WhatsMyName Web](https://whatsmyname.app/) is an incredible way to find someone if you know their username or have their username from a platform.
- [OSINT Framework](https://osintframework.com/) helps you visualize the OSINT process and how to build a profile on someone.
- [Sourcing Games](https://sourcing.games/) is a great site for practicing OSINT skills with CTF-esc challenges and puzzles.
- [Censys](https://search.censys.io/) allows you to view the IP, ports, and services that are open for a given website; also allows you to see the vulnerabilities of that website.
- [OSINT4ALL](https://start.me/p/L1rEYQ/osint4all) is a free, easy to use toolkit for OSINT.

[def]: #osint
