# Enterprise Network Architecture & Security Simulation


<img width="280" height="100" alt="image" src="https://github.com/user-attachments/assets/a24aad27-6f3d-421a-b0f7-5449ae1e080c" />


---
Network Security project designed and simulated using Cisco Packet Tracer, demonstrating a **collapsed core star topology enterprise network architecture**. The design focuses on secure segmentation, centralized routing, and controlled inter-department communication using VLANs, ACLs, and firewall enforcement.

All access-layer switches are connected in a star formation to a central Layer 3 core switch, which handles inter-VLAN routing and network policy enforcement.

---

### 👥 Team Members & Responsibilities

This project was a collaborative effort by a team of six members, each with a defined role:

* **Kipras (Topology):** Led the foundational network layout phase, which has been successfully completed. His responsibilities included mapping out the 6 distinct sectors with VLANs, designing the physical layout, and handling cables. Additionally, he created the project landing page and fully documented his actions.
* **Mateo (Server):** Responsible for core server deployment and network addressing, a phase that is now completed. He designed the IP addressing scheme, configured printer services, and set up critical network services including DNS, DHCP, and FTP, alongside completing his corresponding documentation.
* **Sofia (Security A):** Tasked with establishing initial network perimeter security and access controls, a phase currently in progress. Her focus includes the hardware firewall configuration, setting up centralized AAA services, defining VPN/access policies, and logging these implementations in the documentation.
* **Hannah (Security B):** Managing advanced network security defenses, currently in progress. Her core duties involve the implementation of Access Control Lists (ACLs), DMZ configuration, enforcing port security and device hardening, as well as compiling the technical documentation for these actions.
* **Mustafa (Documentation):** Acting as the central archivist and coordinator for the project's final outputs.His responsibilities include developing the Access Control Matrix, organizing IP tables and network diagrams, and overseeing the final PDF compilation of the entire project's paperwork.
* **Madumathi (Admin):** Served as the Project Lead, overseeing all phases from initial planning to final delivery. Madu's responsibilities include managing the administrative, financial, and presentation deliverables of the project—specifically performing the cost estimation and budget management for all network components, preparing the final presentation, and structuring, editing, and compiling the main project documentation.

---

## 🔐 Key Features

- Collapsed Core Star Topology design
- VLAN-based segmentation and isolation
- Inter-VLAN routing via Layer 3 core switch
- Access Control Lists (ACLs) for traffic control
- Edge firewall for perimeter security
- Centralized server services (DNS, DHCP, HTTP, RADIUS)
- Secure enterprise printing (dedicated VLAN)
- Department-wise isolation and security zoning
- Scalable enterprise network design

---

## 🧱 Network Architecture

### Topology Type
**Collapsed Core Star Topology**

### Layers
* **Core Layer (Collapsed Core Switch - Layer 3)**
  * Inter-VLAN routing
  * Central policy enforcement
  * Network backbone connectivity
* **Access Layer (Star Topology)**
  * Multiple Layer 2 switches
  * Each department connects directly to the core switch
* **Edge Layer**
  * Firewall for external traffic control
  * Security boundary enforcement
* **Server Room (MDF)**
  * Central services and infrastructure systems

---

## 🖥️ Network Clusters

* Server Room (Core Services & Storage)
* Production Cluster
* IT Administration Cluster
* Management Cluster
* Support A Cluster
* Support B Cluster
* Study Cluster

---

## 📡 Technologies Used

- Cisco Packet Tracer
- Cisco Layer 2 Switches
- Cisco Layer 3 Switch (Core)
- VLANs & Subnetting
- ACL (Access Control Lists)
- Firewall Security Rules
- DHCP, DNS, HTTP, RADIUS Services

---

## 🚀 Objectives

- Design and implement a secure enterprise network
- Enforce VLAN-based segmentation
- Prevent unauthorized inter-department access
- Centralize routing using a collapsed core switch
- Simulate real-world enterprise security architecture

---

## 📁 Project Structure

```
.
├── README.md                           # Project overview, team roles, and implementation guide
│
├── configs/                            # Network configuration files & master topology
│   ├── Main_Topology.pkt               # The definitive, working Packet Tracer file
│   ├── core-switch-config.txt
│   ├── firewall-config.txt
│   ├── server-configs.txt
│   ├── access-switch-configs/
│   │   ├── support-a-switch.txt
│   │   ├── support-b-switch.txt
│   │   ├── production-switch.txt
│   │   ├── study-switch.txt
│   │   ├── management-switch.txt
│   │   └── it-switch.txt
│
├── documentation/                      # All project documentation and admin deliverables
│   ├── Main/                           # Final combined team outputs
│   │   ├── Final_report.pdf
│   │   └── Networking_Analysis.pdf
│   │  
│   ├── Admin/                          # Madu's budget and presentation files
│   │   ├── cost_estimation.xlsx
│   │   └── presentation.pptx
│                 
└── screenshots/                        # Visual verification of tests and setups
    ├── topology-overview.png
    ├── vlan-segmentation.png
    ├── firewall-setup.png
    └── ping-tests.png
```
---
## 🖼️ Screenshots
Below are the visual verifications of the implemented network architecture. All source images can be found in the /screenshots directory.

Complete Topology View
VLAN Segmentation Map
Firewall Configuration
Connectivity Test Results (Ping/Traceroute)

## ⚙️ How to Run the Project
Follow these steps to open and validate the network simulation:

1. Prerequisites: Ensure you have Cisco Packet Tracer installed (v8.2 or higher recommended).

2. Clone the Repository:
```
Bash
git clone [https://github.com/](https://github.com/)[your-username]/BXL-Hamilton-2026-Netify
cd BXL-Hamilton-2026-Netify
```
3. Load the Simulation: Open Cisco Packet Tracer, navigate to File > Open, and select the master file:

```
configs/Main_Topology.pkt
```
4. Initialization: Wait 1–2 minutes for the STP (Spanning Tree Protocol) convergence and routing protocols to transition from amber to green.

5. Verification Steps:

-  Verify VLAN assignments on the access switches (configs/access-switch-configs/).

-  Verify DHCP allocation on the end-user workstations (ensure no APIPA 169.254.x.x addresses).

-  Test Inter-VLAN routing across permitted departments based on the IP plan.

-  Verify Firewall rules by attempting to access restricted zones.

6. Connectivity Testing: Open the CLI on any end-device host and execute:
```
ping [target_ip]

tracert [target_ip]
```
---

## 🔐 Security Design Summary
- The architecture implements defense-in-depth principles across multiple layers:

- VLAN Isolation: Strict layer-2 segmentation separating distinct department zones (Support A, Support B, Production, Study, Management, and IT).

- Controlled Inter-VLAN Routing: Enforced via strict IP Access Control Lists (ACLs) to ensure only authorized traffic crosses segment boundaries.

- Perimeter Defense: Hardware firewall filtering acting as a gateway barrier for external and edge traffic.

- Centralized Authentication: AAA/RADIUS-ready design for unified device administration and identity control.

- Server Hardening: Critical enterprise servers (DNS, DHCP, FTP) are isolated within a dedicated, highly protected network zone.
---
## 📊 Outcome
This project demonstrates a fully functional enterprise network with:

- Scalability: Built on a robust collapsed core star topology capable of enterprise expansion.
- Zero-Trust Trajectory: High-level segmentation and isolation between sensitive business units.
- Secure Collaboration: Granular, controlled inter-department communication pathways.
- Centralized Services: Unified routing, DHCP, and DNS management.
- Real-world Implementation: Emulates genuine enterprise security baselines.
---
## 📌 License
This repository is an Educational / Academic Cisco Packet Tracer Simulation Project. It is intended solely for instructional and portfolio demonstration purposes.
