# **Day#13: Detecting and Removing Malicious Cron Jobs – Linux Incident Response Lab**

---

## 🎯 **Objective:**  
The objective of this lab is to investigate and respond to a **malicious cron job** used by an attacker to maintain persistence on a Linux system. Students will simulate the attack, detect the malicious scheduled task, analyze the script, and remove the threat — applying the full incident response lifecycle.


## 📘 **What is a Cron Job?**

A **cron job** is a scheduled task that runs automatically at defined intervals on Unix/Linux systems. Attackers often use cron to **re-execute payloads**, reconnect to command-and-control servers, or maintain access to a compromised system.

---

## 🛠️Key Features:
- Run commands automatically (e.g., every minute, daily, weekly)
- Useful for backups, updates, monitoring scripts, etc.
- Works in the background via the cron service

## 🧾Format of a crontab entry:

```
*  *  *  *  *  command-to-run
│  │  │  │  │
│  │  │  │  └─ Day of the week (0-7, Sun = 0 or 7)
│  │  │  └──── Month (1 - 12)
│  │  └─────── Day of month (1 - 31)
│  └────────── Hour (0 - 23)
└───────────── Minute (0 - 59)
```


## 🔁 **Incident Response Process (NIST SP 800-61 Rev. 2)**

| **Phase**                         | **Description**                                                                 |
|----------------------------------|---------------------------------------------------------------------------------|
| **1. Preparation**               | Ensure system logging is active and users are trained to detect unusual cron behavior. |
| **2. Detection and Analysis**    | Identify unauthorized cron entries and investigate associated scripts or IP addresses. |
| **3. Containment, Eradication, and Recovery** | Stop the malicious cron activity, remove the script, and restore system configuration. |
| **4. Post-Incident Activity**    | Document the incident, and set alerts for future cron job changes.              |

---

## ⚠️ **Scenario: A Malicious Cron Job is Running Every Minute**

An attacker has added a cron job that silently runs a malicious script from `/tmp` every minute. Your job is to detect it, understand its behavior, and remove it safely.

---

## 🛠️ **Lab Setup**

### **System Requirements:**
- Ubuntu 20.04/22.04 or Kali Linux
- Terminal with sudo access

## **Simulate the Incident:**

1. Create a fake "malicious" script:
```bash
echo -e '#!/bin/bash\necho "Ping from attacker server" >> /tmp/.cron.log' > /tmp/malicious.sh
chmod +x /tmp/malicious.sh
```
2. Add a cron job for the current user:
```
echo "* * * * * /tmp/malicious.sh" >> /var/spool/cron/root
```


## Lab Checklist

✅ Simulate Cron Job	Create a malicious script and schedule it via cron
✅ Investigate	Detect the cron job and examine the script behavior
✅ Respond	Remove the script and the cron entry
✅ Document	Record all findings and suggest prevention steps

## 📸 Submission
Submit screenshots showing:
- crontab -l output with the malicious job
- Contents of the cron script /tmp/malicious.sh
- Logs confirming the script execution
- Cleaned cron job list and deletion confirmation

- -----------------------------------------------------------------------------------------------------------------------------------------
###Output of Task - 13

* In this task - 13 am just learn what cron job and its and how attacker use cron to the victim
* As a soc analyst how to detect, Analyze, Investigate and respond to cron based script execution.

![Screenshot 2025-04-30 144851](https://github.com/user-attachments/assets/c5212854-6cce-4a89-a974-28f41113b9ed)

![Screenshot 2025-04-30 144909](https://github.com/user-attachments/assets/48befc5f-e667-47a8-9f72-bdac70232d48)

![Screenshot 2025-04-30 144934](https://github.com/user-attachments/assets/3033ec4f-15bd-4748-9924-7674a54910d9)

--------------------------------------------------------------------------------------------------------------------

Completed Task - 13 

---------------------------------------------------------------------------------------------------------------------













