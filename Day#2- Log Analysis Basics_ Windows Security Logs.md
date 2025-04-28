# **Day#2: Log Analysis Basics: Windows Security Logs**

## **Objective:**
The objective of this lab is to introduce students to **Windows Security Logs** and help them understand how to analyze logs for security-related events. Students will learn how to explore and analyze various security logs such as login attempts, user account changes, and other critical system events that could indicate potential security threats.


## **Lab Setup**
### **Requirements:**
- **System:** Windows 10/11 or Windows Server 2019/2022
- **Tools:**
  - **Windows Event Viewer** (pre-installed)
  - **Notepad** (to create custom events, if needed)
  - **Administrative Privileges** (to access certain security logs)

---

## **What are Windows Security Logs?**
Windows Security Logs contain records of security-related events on the system, such as:
- **Successful and Failed Login Attempts:** Track users who log in or fail to log in.
- **Account Lockouts:** Occurs when a user exceeds the maximum allowed number of incorrect login attempts.
- **Audit Policies:** Logs related to changes in system audit settings and configurations.
- **Group Membership Changes:** Tracks changes in group memberships and user privileges.
- **Privilege Escalation:** Logs events when a user gains elevated privileges.

These logs are valuable for monitoring security incidents, detecting unauthorized access, and auditing system changes.

---

## **Understanding Event IDs in Security Logs:**
Some common **Event IDs** in **Windows Security Logs** that you will encounter include:
- **Event ID 4624**: Successful Logon.
- **Event ID 4625**: Failed Logon.
- **Event ID 4740**: Account Lockout.
---

## **Lab Task: Explore and Analyze Windows Security Logs**


### **Step 1: Simulate a Failed Login Attempt**
1. Create a test user name "haxuser1" on Windows machine.
2. Simulate a failed account access using this command
   Open **PowerShell** and enter an invalid username and password. You can do this by using the following command:
   ```cmd
   net use \\127.0.0.1\IPC$ /user:haxuser1 WrongPassword
   ```
   Here:
   
| Command Part           | Explanation                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| `net use`              | A command used to connect to shared resources (like network shares or printers).              |
| `\\127.0.0.1\IPC$`     | A special hidden administrative share called `IPC$` on your local machine (127.0.0.1 = localhost). `IPC$` is used for inter-process communication, especially for authentication purposes. |
| `/user:haxuser1`       | Specifies the username to use for authentication (in this case, `haxuser1`).                 |
| `WrongPassword`        | The password you're trying to authenticate with — which is intentionally incorrect.           |

Or Else you can sign out with your existing account and sign in with `haxuser1` account with an invalid password



### **Step 2: Detect the Log in Windows Event Viewer**
1. In the **Event Viewer**, navigate to:  
   `Windows Logs → Security`
2.  After the failed login, go back to Event Viewer.
3. Filter the Security Logs for Event ID 4625 (Failed Logon).
4.. Look for entries that correspond to the failed login attempt.
5. Take a screenshot of the event details, including:
   - Failed Login Attempt Details
   - User Name
   - Logon Type
   - Source Network Address

## Conclusion:
- Understanding Windows Security Logs: Windows Security Logs are essential for identifying suspicious behavior such as unauthorized login attempts, privilege escalation, and system configuration changes.
- SOC Analyst Role: As a SOC Analyst, reviewing and analyzing these logs regularly is critical to detecting and responding to security incidents in real-time.
- Threat Detection: By monitoring for multiple failed logins, account lockouts, and privilege escalations, SOC Analysts can quickly detect malicious activities on a network.

## Submission:
- Event ID 4624 (Successful Login): Submit a screenshot showing a successful login event from the Security logs.
- Event ID 4625 (Failed Login): Submit a screenshot showing a failed login attempt event from the Security logs.
- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Output of Task-3
----------------------

* In this task am just learn what is successful and failed login attempt and it may indicate potential threat or unauthorized access. As a SOC Analyst how to detect and analyze those logs 4625, 4624 on windows (event viewer) and respond to unauthorized access to protect our orgainsations IT Infrastructure.

* Successful Login Attempt on Splunk :

![Screenshot 2025-04-25 112657](https://github.com/user-attachments/assets/92608bb3-67aa-4fff-b2bf-f6a862ce1844)

* Successful Login Attempt on Windows :

![Screenshot 2025-04-28 171857](https://github.com/user-attachments/assets/89ad9ae0-6e32-4c39-bb05-be871ef2b03c)

* Failed Login Attempt on Splunk :

![Screenshot 2025-04-25 112641](https://github.com/user-attachments/assets/c4f8aec7-d827-481d-9cb2-52218546d928)


* Failed Login Attempt on Windows :
![Screenshot 2025-04-28 171919](https://github.com/user-attachments/assets/60b042dc-267b-4165-84a0-d7994d077aff)


--------------------------------------------------------------------
   Completed Task-2
   -----------------------------------------------------------



