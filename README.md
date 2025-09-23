




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

[def]: #osint
