# **Day#9: Wireshark Basics – HTTP Protocol Analysis**

---

## 🎯 **Objective**  
The objective of this lab is to help students analyze **HTTP (Hypertext Transfer Protocol)** packets using **Wireshark**. Students will explore HTTP request/response headers, understand how web communication works, and learn how to detect common HTTP-based attacks or data leaks.


## 🛠️ **Lab Setup**

### **System Requirements**
- **Operating System:** Windows 10/11 (or Linux/macOS)
- **Software:** Wireshark (latest version)

## 📘 **HTTP Packet Structure and Fields**

HTTP is an **application-layer protocol** used for communication between clients (browsers) and web servers. It typically runs over TCP port **80**.

### **Key HTTP Fields:**

| Field Name         | Description                              |
|--------------------|------------------------------------------|
| **Request Method** | GET, POST, HEAD, etc.                    |
| **Host**           | The website being accessed               |
| **User-Agent**     | Information about the client/browser     |
| **URI**            | Resource path on the server              |
| **Status Code**    | Server's response status (e.g., 200 OK)  |
| **Content-Type**   | MIME type of the response (e.g., text/html) |
| **Cookie/Header**  | Session or tracking information          |

---

## ✅ Conclusion
- HTTP traffic is readable and easy to analyze in Wireshark.
- Analyzing HTTP helps detect:
 - Sensitive data exposure in URLs or headers
 - Malware beaconing to C2 servers
 - Suspicious file downloads or unauthorized access

## 📸 Submission
Submit a screenshot showing:
- Show all HTTP traffic
- Show all GET requests
- View requested resources





-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Output of Task - 9
-------------------------

* HTTP Stands for Hyper Text Transfer Protocol
* HTTP is less secure because its sent data and retrive data through plain sheet.

Show all HTTP traffic
-------------------------
![Screenshot 2025-04-30 103841](https://github.com/user-attachments/assets/6361f4b0-cc42-4bd5-bc7a-4842d312b4fe)

Show all GET requests
----------------------

![Screenshot 2025-04-30 104107](https://github.com/user-attachments/assets/1338df15-5d50-4049-9f8d-62aedd96f316)


View requested resources
----------------------------

![Screenshot 2025-04-30 104421](https://github.com/user-attachments/assets/a0eb93ed-ad2b-44fe-a5ce-7027100b3d0f)


=================================================================================================================================

              Completed Task - 9 

 ======================================================================================================================================























  
