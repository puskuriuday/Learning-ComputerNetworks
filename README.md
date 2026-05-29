# CISCO-Learn

My personal learning repository for the **Cisco CCNA 200-301** certification, following [Jeremy's IT Lab](https://www.youtube.com/@JeremysITLab) free CCNA course on YouTube.

This repo holds my completed Packet Tracer lab files, configuration notes, and study progress as I work through the full course.

---

## About the Course

**Jeremy's IT Lab — Free CCNA 200-301 Complete Course**

- **Instructor:** Jeremy Cioara (Jeremy's IT Lab)
- **Certification Target:** Cisco Certified Network Associate (CCNA) 200-301
- **Course Format:** Video lectures + hands-on Packet Tracer labs + practice quizzes + flashcards
- **Cost:** 100% Free
- **Playlist:** [Free CCNA 200-301 | Complete Course](https://www.youtube.com/playlist?list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ)

The course covers everything needed for the CCNA exam, including:

- Network fundamentals (OSI/TCP-IP models, cables, topologies)
- Ethernet LAN switching (VLANs, STP, EtherChannel)
- IP addressing (IPv4, IPv6, subnetting)
- Routing (static, OSPF, routing tables)
- Wireless networking
- Network security (ACLs, port security, DHCP snooping)
- Network automation and programmability
- Services (DHCP, DNS, NAT, NTP, SNMP, Syslog)

---

## Tools Used

| Tool | Purpose | Stage |
|------|---------|-------|
| **Cisco Packet Tracer** | Cisco-built network simulator for the Jeremy's IT Lab labs | Primary — entire course |
| **Linux Networking Lab** (`~/Desktop/setup`) | Real Linux networking using namespaces, `ip`, `tcpdump`, etc. | Supplementary — after Day 15 |
| **GNS3** | Advanced simulator that runs real Cisco IOS firmware | Post-CCNA / CCNP prep |
| **YouTube** | Jeremy's IT Lab video lectures | Daily |
| **Anki / Flashcards** | Spaced repetition for memorization | Daily |
| **Boson ExSim** *(optional, paid)* | Practice exams before sitting CCNA | Final 2-3 weeks |

### Installing Packet Tracer
Packet Tracer is free via the [Cisco Networking Academy](https://www.netacad.com/courses/packet-tracer). Register a free account, then download the latest version for your OS.

---

## Tool Comparison: Packet Tracer vs Linux Setup vs GNS3

Three different tools, three different jobs. Quick decision guide:

| | Packet Tracer | Linux Setup (`~/Desktop/setup`) | GNS3 |
|---|---|---|---|
| **Realism** | Simulated Cisco | Real Linux kernel | Real Cisco IOS firmware |
| **Cisco IOS syntax** | Yes (simulated) | No | Yes (real) |
| **Linux / cloud skills** | No | Yes | No |
| **Resource needs** | Light | Light | Heavy (8 GB+ RAM) |
| **Setup effort** | Easy | Medium (sudo + scripts) | High (need IOS images) |
| **Best for** | CCNA exam prep | Real-world infra / DevOps | CCNP / CCIE / advanced labs |
| **CCNA exam aligned** | Yes | No (concepts only) | Yes |

**My take:**
- **Packet Tracer** wins for following this course — the labs are built for it, the CCNA exam tests Cisco IOS, and Jeremy uses it.
- **The `setup` folder** teaches more *practical* skill per hour — real Linux networking is what production infra actually runs on. Use it to reinforce concepts after they click in Packet Tracer.
- **GNS3** is overkill for CCNA. Pick it up later when chasing CCNP or building enterprise-grade labs.

Don't try to use all three at once — it splits focus and slows progress.

---

## Repository Structure

```
CISCO-Learn/
├── README.md                                    # This file
├── Day 01 Lab - Packet Tracer Introduction.pkt  # Lab 1 - Intro to Packet Tracer
├── Day 02 Lab - Connecting Devices.pkt          # Lab 2 - Connecting end devices
├── Day 03 Lab - OSI Model.pkt                   # Lab 3 - OSI Model simulation
└── ...                                          # More labs as I progress
```

Each `.pkt` file is a Cisco Packet Tracer save file. Open it in Packet Tracer to inspect the topology, configurations, and verify the lab.

---

## Progress Tracker

Course is broken into "Days" — one topic per day. I'm checking them off as I complete them.

### Module 1: Network Fundamentals

- [x] **Day 01** — Introduction to Packet Tracer
- [x] **Day 02** — Connecting Devices
- [x] **Day 03** — OSI Model
- [ ] **Day 04** — Network Topology Architectures
- [ ] **Day 05** — TCP/IP Suite & OSI Model
- [ ] **Day 06** — Binary, Hex, and IP Addressing
- [ ] **Day 07** — Subnetting Part 1
- [ ] **Day 08** — Subnetting Part 2
- [ ] **Day 09** — Subnetting Part 3
- [ ] **Day 10** — The Life of a Packet
- [ ] **Day 11** — Cisco IOS Part 1
- [ ] **Day 12** — Cisco IOS Part 2
- [ ] **Day 13** — Ethernet LAN Switching Part 1
- [ ] **Day 14** — Ethernet LAN Switching Part 2
- [ ] **Day 15** — IPv6 Part 1

### Module 2: Switching, Routing, and Wireless

- [ ] **Day 16** — Routing Fundamentals
- [ ] **Day 17** — Static Routing
- [ ] **Day 18** — VLANs Part 1
- [ ] **Day 19** — VLANs Part 2
- [ ] **Day 20** — DTP & VTP
- [ ] **Day 21** — Spanning Tree Protocol (STP) Part 1
- [ ] **Day 22** — Spanning Tree Protocol (STP) Part 2
- [ ] **Day 23** — Rapid STP
- [ ] **Day 24** — EtherChannel
- [ ] **Day 25** — Dynamic Routing
- [ ] **Day 26** — OSPF Part 1
- [ ] **Day 27** — OSPF Part 2
- [ ] **Day 28** — OSPF Part 3
- [ ] **Day 29** — First Hop Redundancy (HSRP)
- [ ] **Day 30** — TCP & UDP

*(Continuing through Day 60+ — full list updated as I progress.)*

---

## Lab Notes

I'll keep short notes per lab here for quick recall.

### Day 01 — Packet Tracer Introduction
- Got familiar with the Packet Tracer interface, device categories, and how to drag/drop devices.
- Practiced placing PCs, switches, and routers.
- Learned the difference between **Logical** and **Physical** workspaces.
- Used the **Simulation Mode** to visualize packet flow step by step.

### Day 02 — Connecting Devices
- Connected end devices (PCs) to a switch using straight-through copper cables.
- Connected switches together using crossover cables (or auto-MDIX).
- Learned which cable type goes with which device pair:
  - **Straight-through:** PC <-> Switch, Router <-> Switch
  - **Crossover:** PC <-> PC, Switch <-> Switch, Router <-> Router, PC <-> Router
  - **Serial (DCE/DTE):** Router <-> Router (WAN simulation)
- Assigned IP addresses to PCs and tested connectivity using `ping`.

### Day 03 — OSI Model
- Walked through all 7 layers of the OSI model and what each one is responsible for:
  - **Layer 7 — Application:** User-facing protocols (HTTP, FTP, DNS, SMTP)
  - **Layer 6 — Presentation:** Encoding, encryption, compression (TLS/SSL, JPEG)
  - **Layer 5 — Session:** Establishing/maintaining/terminating sessions
  - **Layer 4 — Transport:** End-to-end delivery, segmentation (TCP, UDP, port numbers)
  - **Layer 3 — Network:** Logical addressing & routing (IP, ICMP, routers)
  - **Layer 2 — Data Link:** Framing & MAC addressing (Ethernet, switches)
  - **Layer 1 — Physical:** Bits over wire/wireless (cables, signals, NICs)
- Used Packet Tracer's **Simulation Mode** to capture a packet and step through it layer by layer — watching encapsulation add headers on the way down and decapsulation strip them on the way up.
- Mapped each Packet Tracer device to its OSI layer (hub = L1, switch = L2, router = L3).
- Memorized mnemonic: *"Please Do Not Throw Sausage Pizza Away"* (L1 → L7) and *"All People Seem To Need Data Processing"* (L7 → L1).
- Saw the difference between **OSI** (7 layers, theoretical) and **TCP/IP** (4 layers, practical).

---

## Useful Cisco IOS Commands (Cheat Sheet)

Commands I keep coming back to. Will grow over time.

### Basic Navigation
```
enable                          # Enter privileged EXEC mode
configure terminal              # Enter global configuration mode
exit                            # Move down one mode
end                             # Jump straight to privileged EXEC
?                               # Show available commands / completions
```

### Show Commands
```
show running-config             # Active configuration in RAM
show startup-config             # Saved configuration in NVRAM
show ip interface brief         # Summary of interfaces & IPs
show interfaces                 # Detailed interface stats
show version                    # IOS version, uptime, hardware info
show mac address-table          # Switch MAC address table
show vlan brief                 # VLAN summary
```

### Saving Configuration
```
copy running-config startup-config       # Save config
write memory                             # Same thing, shorthand
```

### Interface Configuration
```
interface GigabitEthernet0/1
 ip address 192.168.1.1 255.255.255.0
 no shutdown
 description LINK TO SWITCH1
```

---

## Study Approach

The way I'm working through the course:

1. **Watch the day's video** in full, taking written notes.
2. **Re-watch** any sections that didn't click.
3. **Do the lab** in Packet Tracer without looking at the solution first.
4. **Compare** my solution to Jeremy's walkthrough.
5. **Save the `.pkt` file** to this repo and tick the checkbox above.
6. **Do the flashcards / quiz** for that day to lock in the knowledge.

Goal is to finish all 60+ days and then take 2-3 weeks of dedicated practice exams (Boson ExSim) before sitting the real exam.

---

## Useful Links

- [Jeremy's IT Lab — Official Website](https://www.jeremysitlab.com/)
- [Free CCNA Playlist on YouTube](https://www.youtube.com/playlist?list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ)
- [Anki Flashcard Deck (free)](https://www.jeremysitlab.com/anki-flashcards)
- [Practice Quizzes (free)](https://www.jeremysitlab.com/free-ccna-quiz-questions)
- [Cisco CCNA 200-301 Official Exam Topics](https://www.cisco.com/c/dam/en_us/training-certifications/exams/CCNA_200-301_ExamTopics.pdf)
- [Packet Tracer Download (NetAcad)](https://www.netacad.com/courses/packet-tracer)

---

## License & Credit

All lab content, structure, and exercises are credit to **Jeremy Cioara** of Jeremy's IT Lab. This repo only contains my personal completed lab files and study notes — not the original course material.

If this course helped you, consider supporting Jeremy on his [YouTube channel](https://www.youtube.com/@JeremysITLab) or [Patreon](https://www.patreon.com/JeremysITLab).
