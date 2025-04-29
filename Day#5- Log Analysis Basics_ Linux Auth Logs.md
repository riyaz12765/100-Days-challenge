# **Day#5: Log Analysis Basics – Linux Auth Log**

---

## 🎯 **Objective**  
The objective of this lab is to simulate an **SSH brute force attack** and demonstrate how to detect it using **Linux authentication logs**. Students will learn how to identify multiple failed login attempts and analyze patterns to uncover brute force activity.


## 🛠️ **Lab Setup**

### **System Requirements**
- **Attacker Machine:** Kali Linux (or any Linux with `hydra`)
- **Target Machine:** Ubuntu Linux Server

### **Tools Needed**
- `hydra` (on attacker machine)
- `openssh-server` (on target machine)
- `rsyslog` (default logging service)

### **Log Files**
- `/var/log/auth.log` – Authentication logs (Ubuntu/Debian)
- `/var/log/secure` – (CentOS/RHEL)

---

## 📘 **Preparation**

Linux systems log every authentication event, including successful and failed SSH login attempts. Brute force attacks can be identified by analyzing patterns such as:
- Rapid failed logins from a single IP
- Attempts with multiple usernames
- Login successes after a string of failures

---

## 🧠 **What is an SSH Brute Force Attack?**

A **brute force attack** attempts to guess a user’s SSH password by trying many combinations quickly using automated tools like Hydra.

### **Why It’s Dangerous**
- Successful brute force = full shell access  
- Attackers can pivot, install malware, or exfiltrate data  
- It often goes unnoticed without proper log monitoring

---

## 🛡️ **Attack Patterns Detectable via Auth Logs**
- Multiple failed password attempts from one IP
- Repeated login attempts to root/admin accounts
- Success after multiple failures (brute force success)
- Logins from unknown or foreign IPs

---

## What is Hydra?
- Hydra is a fast, open-source password-cracking tool used for brute force attacks on logins.
- It supports 50+ protocols like SSH, FTP, HTTP, SMB, and more.
- Common use: penetration testing and checking for weak passwords in network services.
- Syntax: `hydra -L users.txt -P passlist.txt <target_ip> <protocol>`
- Use `-l/-p` for single username/password or `-L/-P` for files.
- Add `-vV` for verbose output and `-t 4` to set number of threads.

## 🧪 **Lab Task: Explore and Analyze Auth Logs for SSH Brute Force**

---

### ⚔️ **Step 1: Attack Simulation – Brute Force SSH using Hydra**

> ⚠️ *Only perform on authorized systems you own or control.*

**On the Attacker Machine:**
```bash
hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://TARGET-IP
```
This will attempt multiple password guesses for user root on the SSH port.

Ensure SSH is enabled on the target:
```
sudo systemctl status ssh
```
### 🔍 Step 2: Detection and Analysis – Analyze Auth Logs
Check for failed login attempts:
```
sudo grep "Failed password" /var/log/auth.log
```
Find usernames tried:

```
sudo grep "Failed password" /var/log/auth.log | awk '{print $(NF-5)}' | sort | uniq -c | sort -nr
```
Watch live log activity:

```
sudo tail -f /var/log/auth.log
```

### 🔍 What to Look For
- 20+ failed attempts from the same IP in under 5 mins
- Attempts on sensitive users (root, admin)
- Sudden success after multiple failures

## ✅ Conclusion
- Auth logs are vital for detecting brute force login attempts
- Multiple failures from a single IP is a strong signal of attack
- Combine log analysis with tools like fail2ban to block repeat offenders automatically

## 📸 Submission
Submit a screenshot showing:
- failed login entries from the same IP
- Username attempted

- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Output of Task - 5
------------------------

* In this task - 5 am lust learn brute force attack and how its works and as a soc analyst how to detect and analyze those logs and investigate. 
* Before Simulating a attack we need to extract the file rockyou.txt.

![Screenshot 2025-04-29 114803](https://github.com/user-attachments/assets/46fe8eb7-4d9c-4d7f-8c0a-670dbf4fbeb3)

* Finally we can see logs under /var/log/auth.log which is generating by attacker machine IP is 192.168.81.130 and it could indicate brute force attack multiple failed login from single ip.


![Screenshot 2025-04-29 114719](https://github.com/user-attachments/assets/9ae9eea1-6112-41f1-a366-723f00d8fffb)



![Screenshot 2025-04-29 114708](https://github.com/user-attachments/assets/e2c5c2fa-b4e0-4bdd-96a3-069a83f49640)


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                              Completed Task - 5 
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------







