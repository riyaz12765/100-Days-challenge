# **Day#8: Wireshark Basics – TCP Protocol Analysis**

---

## 🎯 **Objective**  
The objective of this lab is to introduce students to analyzing **TCP (Transmission Control Protocol)** traffic using **Wireshark**. Students will learn how TCP establishes connections, the 3-way handshake process, and how to interpret common TCP fields and flags.

## 🛠️ **Lab Setup**

### **System Requirements**
- **Operating System:** Windows 10/11 (or Linux/macOS)
- **Software:** Wireshark (latest version)


## 📘 **TCP Packet Structure and Fields**

TCP is a **Layer 4 (Transport Layer)** protocol that ensures reliable, ordered, and error-checked delivery of data between applications.

### **Key TCP Fields:**

| Field Name         | Description                                  |
|--------------------|----------------------------------------------|
| **Source Port**     | Sender’s port number                         |
| **Destination Port**| Receiver’s port number                       |
| **Sequence Number** | Number of the first byte in the segment      |
| **Acknowledgment No** | Confirms received data                    |
| **Flags**           | Control bits (SYN, ACK, FIN, RST, PSH, URG) |
| **Window Size**     | Buffer size available                        |
| **Checksum**        | Error-checking field                         |

## ✅ Conclusion
- TCP ensures reliable and ordered data delivery through its 3-way handshake and flow control.
- Understanding TCP flags is essential for:
 - Connection state tracking
 - Troubleshooting dropped or reset connections
 - Detecting scanning and abnormal behavior (e.g., RST floods)

## Submission
Submit a screenshot showing:
- Show all TCP packets
- Show SYN packets (start of connection)
- Show FIN packets (end of connection)
- TCP traffic to/from a specific host



============================================================================================================================================================================================================================

###Output of Task - 8
---------------------
* TCP stands for Transmission Control Protocol
* TCP Ensure Reliable data transmission with eroor checking, Flowcontrol.

 1] Show all TCP packets


![Screenshot 2025-04-29 184656](https://github.com/user-attachments/assets/e8a60208-5e72-4aa4-aa73-e2a012d3d5fe)


2] Show SYN packets (start of connection)

![Screenshot 2025-04-29 184727](https://github.com/user-attachments/assets/1415a1dc-e53a-4c5b-a9a6-a1d1f426e9f7)


3]  Show FIN packets (end of connection)

![Screenshot 2025-04-29 184817](https://github.com/user-attachments/assets/e836062a-5d69-4b48-9c99-36e961669e74)


4] TCP traffic to/from a specific host


![Screenshot 2025-04-29 184858](https://github.com/user-attachments/assets/a8b37bf7-2122-4bab-8ce7-001abfac5a22)

====================================================================================================================================================================================================================
               Completed Task - 8
=====================================================================================================================================================================================================================






























 
