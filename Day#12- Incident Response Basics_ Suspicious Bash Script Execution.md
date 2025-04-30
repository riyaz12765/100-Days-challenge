# **Day#12: Incident Response Basics – Linux Suspicious Bash Script Execution**

---

## 🎯 **Objective:**  
The objective of this lab is to help students understand the **core steps of incident response** by investigating a **suspicious bash script execution** on a Linux system. Students will learn how to detect, analyze, and respond to a basic script-based intrusion.

---

## 📘 **What is Incident Response?**

**Incident Response (IR)** is the process of detecting and managing a cybersecurity incident to minimize impact and restore normal operations. This lab introduces a basic Linux scenario where an attacker’s script is executed through user error or misconfiguration.

---

## 🔁 **Incident Response Process (NIST SP 800-61 Rev. 2)**

| **Phase**                         | **Description**                                                                 |
|----------------------------------|---------------------------------------------------------------------------------|
| **1. Preparation**               | Ensure logging is enabled, tools are installed, and the system is ready.        |
| **2. Detection and Analysis**    | Identify suspicious activity using logs, running processes, and file checks.    |
| **3. Containment, Eradication, and Recovery** | Isolate the threat, remove the script, and secure the system.                    |
| **4. Post-Incident Activity**    | Document the incident and implement prevention steps.                          |

---

## ⚠️ **Scenario: Suspicious Script Found in /tmp**

Your monitoring system flagged a suspicious file in `/tmp`. Upon inspection, it's a bash script (`payload.sh`) that connects to an unknown IP. You are tasked with investigating this incident.

---

## 🛠️ **Lab Setup**

### **System Requirements:**
- Ubuntu 20.04/22.04 or Kali Linux
- Terminal access with sudo privileges

### **Simulate teh attack:**

1. Create a test directory:
```
mkdir ~/script-lab && cd ~/script-lab
```
2. Create a Bash script:

```
nano fakebackup.sh
```
3. Paste the following content:

```
#!/bin/bash
echo "[*] Simulating backup operation..."
sleep 60
```
4. Make the script executable:

```
chmod +x fakebackup.sh
```

5.  Simulate the Attack / Execution
Run the script in the background:
```
./fakebackup.sh &
```


## Lab Checklist
✅ Simulate Script	Create and execute a suspicious bash script    
✅ Investigate Logs	Use commands to analyze the event    
✅ Kill and Delete	Contain and remove the malicious file   
✅ Document Findings	Note IPs, users, and recommendations    

## 📸 Submission
Submit screenshots of:
- The malicious script content    
- Process list showing the script or curl
- Script deleted from /tmp

- ------------------------------------------------------------------------------------------------------


### Output of Task - 12
---------------------------

* In this task - 12 am just learn as a attacker how execute the bash script and as a soc anlyst how to detect, analyze, investigate, respond include kill the process and remove the script.

![Screenshot 2025-04-30 140043](https://github.com/user-attachments/assets/709bfeb8-48e4-45cb-94f5-14d69fcefbc4)


![Screenshot 2025-04-30 140057](https://github.com/user-attachments/assets/f5fbd745-6d2b-4254-82f0-5efbb6d9d66a)

--------------------------------------------------------------------------------------------------------------------
       Completed task - 12

 -----------------------------------------------------------------------------------------------------------------





















