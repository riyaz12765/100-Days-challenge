# **Day#10: Wireshark Basics – TLS Protocol Analysis**

---

## 🎯 **Objective**  
The objective of this lab is to help students analyze **TLS (Transport Layer Security)** traffic using **Wireshark**. Students will explore how TLS secures data over the network, understand handshake messages, and identify metadata like server names and certificate details.

---

## 🛠️ **Lab Setup**

### **System Requirements**
- **Operating System:** Windows 10/11 (or Linux/macOS)
- **Software:** Wireshark (latest version)


## 📘 **TLS Packet Structure and Fields**

TLS is a **cryptographic protocol** that provides secure communication over the internet. It runs over **TCP**, commonly on port **443**, and is used in HTTPS, FTPS, SMTPS, etc.

### **Key TLS Handshake Messages:**

| Message Type          | Description                                      |
|------------------------|--------------------------------------------------|
| **Client Hello**       | Client initiates secure connection, offers cipher suites |
| **Server Hello**       | Server selects cipher and provides certificate  |
| **Certificate**        | Server provides digital certificate (X.509)     |
| **Key Exchange**       | Client and server exchange keys for session     |
| **Finished**           | Secure session begins                           |


✅ Conclusion
- TLS secures communication using encryption, making traffic unreadable without keys.
- Wireshark can't decrypt TLS by default but can reveal:
 - Server name (SNI)
 - Certificate chain
 - TLS versions and cipher suites

- Analyzing TLS metadata helps detect:
 - Outdated TLS versions (e.g., TLS 1.0)
 - Suspicious or self-signed certificates
 - Malicious domain encryption abuse

## 📸 Submission
Submit a screenshot showing:
- Show all TLS traffic
- Show Client Hello messages
- Show TLS 1.2 traffic
 =========================================================================================

- ### Output of Task - 10
- ------------------------

* TLS Stands for Transport Layer Security
* It its crptographic protocol for encrpted our data over the internet for secure communication.

1] Show all TLS traffic

![Screenshot 2025-04-30 111222](https://github.com/user-attachments/assets/35c3e2b6-3fca-4bc8-8167-850a1e5e0821)

2] Show Client Hello messages

![Screenshot 2025-04-30 111302](https://github.com/user-attachments/assets/360e34a3-bdbc-468e-8e13-7bb3802bcf5d)

3] Show TLS 1.2 traffic

![Screenshot 2025-04-30 111334](https://github.com/user-attachments/assets/2d1ff85a-ad0f-479c-8cc2-209a2311cfad)

-----------------------------------------------------------------------------------------------------------------

   Completed Task - 10
----------------------------------------------------------------------------------------------------------------   



















  

