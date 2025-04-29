# **Day#7: Wireshark Basics – ICMP Protocol Analysis**

---

## 🎯 **Objective**  
The objective of this lab is to help students understand and analyze **ICMP (Internet Control Message Protocol)** packets using **Wireshark**. Students will learn to identify echo requests/replies, interpret ICMP packet fields, and apply relevant filters for investigation.

---

## **▶️Video Tutorial**

[![▶️Watch the video](https://img.youtube.com/vi/K_kPVNjv-7w/maxresdefault.jpg)](https://youtu.be/K_kPVNjv-7w)
---

## 🛠️ **Lab Setup**

### **System Requirements**
- **Operating System:** Windows 10/11 (or Linux/macOS)
- **Software:** Wireshark (latest version)

### **Files Needed**
- [Download Sample PCAP file](https://github.com/0xrajneesh/90-Days-SOC-Challenge-Beginner/raw/refs/heads/main/Protocol_Analysis_pcap.pcapng)

---

## 📘 **ICMP Packet Structure and Fields**

ICMP is a Layer 3 protocol used for sending error messages and operational information. The most common ICMP messages include **Echo Request (Type 8)** and **Echo Reply (Type 0)**.

### **Key ICMP Fields:**

| Field Name       | Description                          |
|------------------|--------------------------------------|
| **Type**         | Defines the ICMP message type        |
| **Code**         | Provides further detail for the type |
| **Checksum**     | Error-checking for header            |
| **Identifier**   | Helps match requests and replies     |
| **Sequence No.** | Sequence of the request/reply        |
| **Data**         | Optional payload                     |

---

## 🔍 **Most Common ICMP Display Filters**

Use these filters in Wireshark’s **Display Filter** bar:

| Filter | Description |
|--------|-------------|
| `icmp` | Show all ICMP traffic |
| `icmp.type == 8` | Show Echo Requests (ping) |
| `icmp.type == 0` | Show Echo Replies |
| `icmp.code == 3` | Destination unreachable |
| `ip.addr == 192.168.1.10` | ICMP traffic from/to specific host |

---

## ✅ Conclusion
- ICMP is a fundamental protocol for network troubleshooting.
- Wireshark helps visualize ICMP packet flow and structure.
- Understanding ICMP helps detect network scanning, ping sweeps, and unreachable hosts.


## 📸 Submission
Submit a screenshot showing:
- ICMP Echo Request and Echo Reply packets


- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Output of Task - 7
-----------------
* ICMP stands for Internet Control Message Protocol
* This protocol helps sent echo request and echo reply.

sent echo request - icmp.type == 8
------------------
![Screenshot 2025-04-29 181020](https://github.com/user-attachments/assets/8090c8cc-56a7-458e-9e82-9259f256b4dd)


echo reply - icmp.type == 0




![Screenshot 2025-04-29 182426](https://github.com/user-attachments/assets/251cb946-0e75-486c-9e14-83647b2ab4e7)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
           Completed Task - 7 
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





