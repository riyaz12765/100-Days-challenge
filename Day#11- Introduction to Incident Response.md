# **Day#11: Introduction to Incident Response**

## **Objective:**
The objective of this lab is to introduce students to the **core concepts of incident response**, familiarize them with the **incident response lifecycle**, and help them understand how basic threats on Windows systems are detected, analyzed, and responded to by SOC Analysts.



## **What is Incident Response?**

**Incident Response (IR)** is the structured approach to handle and manage the aftermath of a **security breach or cyberattack**, also known as an incident. It includes steps to:
- Detect the incident
- Contain the damage
- Investigate the root cause
- Recover normal operations
- Report and document findings

---

## **Incident Response Process (NIST SP 800-61 Rev. 2)**

The NIST Incident Response Lifecycle includes **4 main phases**:

| **Phase**                         | **Description**                                                                 |
|----------------------------------|---------------------------------------------------------------------------------|
| **1. Preparation**               | Establish policies, train team, and set up tools and logging mechanisms.       |
| **2. Detection and Analysis**    | Identify potential incidents using logs, alerts, and anomaly detection systems.|
| **3. Containment, Eradication, and Recovery** | Isolate threats, remove malware/artifacts, and restore systems securely.       |
| **4. Post-Incident Activity**    | Conduct lessons learned, create reports, and improve incident response plans.  |


## **How SOC Analysts Respond to Incidents:**
- Monitor logs and alerts (via SIEM)
- Investigate suspicious behavior
- Contain and isolate infected systems
- Coordinate with other teams
- Document and report the incident

---

## 🧪 Lab Task: Detect and Respond: Windows Server RDP Brute Force Attack

---

## 🧰Lab Setup and Requirements

### 🖥️Machines Required:
- **Windows Server 2019 or 2022**
  - RDP enabled
  - Event Viewer access
  - One local user account with known username
- **Kali Linux VM**
  - Hydra pre-installed
  - Connected to same LAN or Virtual Network

### 📶Network:
- Ensure **both machines are on the same network**
- Verify **RDP (TCP/3389)** is open on Windows Server

---

## ⚙️Preparation Steps

### On **Windows Server**:
1. **Enable RDP**:  
   `System Properties → Remote → Enable Remote Desktop`

2. **Allow RDP in Firewall**:  
   `Windows Defender Firewall → Advanced Settings → Inbound Rules → Remote Desktop (TCP-In) → Enable`

3. **Create Test User**:
   ```powershell
   net user attackerlab Password123 /add
   ```
Open Event Viewer:
Windows Logs → Security
Filter for Event ID 4625 (Failed Logon)



### 🎯Simulate the Attack

1. On Kali Linux:
Install Hydra (if not installed):

```
sudo apt update && sudo apt install hydra
```
Prepare Wordlist: Use the existing list or create a custom one, e.g.: /usr/share/wordlists/rockyou.txt
2. Run this command on Kali Linux:
```
hydra -t 4 -V -f -l attackerlab -P /usr/share/wordlists/rockyou.txt rdp://<Windows_Server_IP>
```
Replace <Windows_Server_IP> with actual IP of Windows Server

### 👁️Visualize the Alert in Event Viewer
1. On Windows Server:
Open `Event Viewer → Windows Logs → Security`

2. Look for Event ID 4625 with:

Logon Type: 10 (RemoteInteractive / RDP)

Failure Reason: "Unknown user name or bad password"

Caller IP Address: IP of Kali machine



### 🚨Incident Response Steps
1. Identify Repeated Failed Logons:
- Spot Event ID 4625 from same IP
2. Correlate IP Address:
- Confirm repeated failures from attacker’s IP
3. Lock the User Account (Optional):
```
net user attackerlab /active:no
```
4. Block Attacker IP:

```
New-NetFirewallRule -DisplayName "Block Attacker" -Direction Inbound -RemoteAddress <Kali_IP> -Action Block
```
5. Collect Evidence:
- Export relevant Event Logs
6. Report Incident:
- Create a brief report with findings and actions taken

## 📩Submission Requirements
Submit the following:
- Screenshot of Hydra attack in Kali Linux
- Screenshot of Event Viewer showing multiple 4625 events
- Firewall rule

## ✅Conclusion
This lab demonstrated how to:
- Simulate an RDP brute-force attack using Hydra
- Detect suspicious logons via Windows Event Viewer
- Respond with basic IR steps without using Sysmon

- -----------------------------------------------------------------------------------------------------------------------------------------
### Output of Task - 11
-------------------------

* In this task - 11 am just learn how to simulate the brute force attack to local user account through remote desktop
* As a soc analyst how to detect and analyse, respond to attacker including block the attacker IP without sysmon.

 Screenshot of Hydra attack in Kali Linux
 ----------------------------------------
 
![Screenshot 2025-04-30 125725](https://github.com/user-attachments/assets/43f4501d-f60f-43b4-af2c-c50844af0d10)

Detect suspicious logons via Windows Event Viewer
---------------------------------------------------

![Screenshot 2025-04-30 122617](https://github.com/user-attachments/assets/6659325c-c4ae-4c62-a363-c93640ccc9bb)


Respond with basic IR steps without using Sysmon
-----------------------------------------------------


![Screenshot 2025-04-30 125924](https://github.com/user-attachments/assets/90284cb3-a721-4f27-8854-a75ac5934066)

----------------------------------------------------------------------------------------------------------------------
   Completed Task - 11

---------------------------------------------------------------------------------------------------------




















