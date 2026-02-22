# Secure Enterprise Network Design
### Routing and Switching Final Project

## 📝 Overview
[cite_start]This project implemented a secure, redundant network for a small enterprise consisting of four departments: Admin, HR, IT, and Finance[cite: 9]. [cite_start]The design focuses on high availability, logical segmentation, and strict access control[cite: 10].

## 🛠️ Key Technical Features
* [cite_start]**Logical Segmentation:** Created 4 distinct VLANs to logically separate departmental traffic[cite: 36].
* [cite_start]**IP Optimization (VLSM):** Implemented VLSM to prevent IP address wastage, providing 10 usable hosts per department[cite: 12, 13].
* [cite_start]**Network Redundancy:** Configured EtherChannel (LACP/Static) using dual links to ensure network stability if a cable fails[cite: 36, 37].
* [cite_start]**Advanced Security:** Applied Extended Access Control Lists (ACLs) to restrict HR, IT, and Finance from talking to each other while allowing Admin full management access[cite: 40].
* [cite_start]**Inter-VLAN Routing:** Enabled `ip routing` on a Multilayer Switch to allow the Admin department to communicate with all sectors[cite: 38].

## 📊 Subnetting Table (VLSM)
| Department | VLAN | IP Range | Gateway | CIDR |
| :--- | :--- | :--- | :--- | :--- |
| **Admin** | 10 | 192.168.10.0 | .1 | /28 |
| **HR** | 20 | 192.168.10.16 | .17 | /28 |
| **IT** | 30 | 192.168.10.32 | .33 | /28 |
| **Finance** | 40 | 192.168.10.48 | .49 | /28 |

[cite_start][cite: 15, 16, 17, 18]

## 🧪 Testing & Results
* [cite_start]**Connectivity:** Verified that the Admin PC successfully pings all other departments[cite: 194].
* [cite_start]**Security:** Pings between HR and Finance resulted in "Destination Host Unreachable," proving ACL effectiveness[cite: 195, 212].
* [cite_start]**Redundancy:** Manually deleting one link in an EtherChannel bundle confirmed traffic continued through the second link[cite: 196, 197].

---
[cite_start]**Developed by:** Daain Akramah Alvi & Umer AL sani Chohan [cite: 3, 4]
