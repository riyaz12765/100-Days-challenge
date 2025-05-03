# Day#18: Splunk Basics – SSH Log Analysis

---

## 🎯 Objective

In this lab, you will:
- Learn how to ingest and analyze SSH logs using Splunk.
- Detect failed and successful SSH authentication attempts.
- Identify unusual SSH activity that may indicate brute force or unauthorized access.

---

## 🖥️ Lab Setup

- ✅ **Splunk**: Already installed and accessible.
- ✅ **Data Source**: JSON-formatted Zeek-style SSH logs.
- 🌐 **Log File**: Download and upload to Splunk using the steps below.

📥 **[Download SSH Log file](https://raw.githubusercontent.com/0xrajneesh/30-Days-SOC-Challenge-Beginner/refs/heads/main/ssh_logs.json)**

---

## ⚙️ Steps to Upload SSH Log into Splunk

1. Go to Splunk Web → **Settings > Add Data**.
2. Choose **Upload** and select `synthetic_zeek_ssh.json`.
3. Set Source type: `json` or create a new one `zeek:ssh`.
4. Index: Choose `main` or create a new index like `ssh_lab`.
5. Finish the upload and confirm indexing.

---

## 🔍 Lab Tasks

Use SPL queries to complete the following analysis:

### ✅Task 1: List the top 10 endpoints with failed SSH login attempts

### ✅Task 2: Find the number of total SSH connections

### ✅Task 3: Count all event types (successful, failed, no-auth, multiple-failed) seen in the logs


## 📸Submission
Submit a screenshot for each of the following:
- Your query and result for Task 1.
- Your query and result for Task 2.
- Your query and result for Task 3.
- --------------------------------------------------------------------------------------------------------------------------------

### Output of Task - 18
------------------------

* Am just learn how to upload the dns.log file into the splunk.
* learn some spl query about splunk to filter needed logs for soc analyst.




Task 1: List the top 10 endpoints with failed SSH login attempts
---------------------------------------------------------------------
![Screenshot 2025-05-03 123202](https://github.com/user-attachments/assets/156823b5-87d4-49af-9558-2c5804370276)

Task 2: Find the number of total SSH connections
------------------------------------------------------
![Screenshot 2025-05-03 123403](https://github.com/user-attachments/assets/3dd8a5b6-9c62-42f4-a93b-1c66255c01d8)


Task 3: Count all event types (successful, failed, no-auth, multiple-failed) seen in the logs
--------------------------------------------------------------------------------------------

![Screenshot 2025-05-03 123700](https://github.com/user-attachments/assets/cd8ca18b-6e51-4eb4-ae93-0231032448d8)

--------------------------------------------------------------------------------------------------------------------------
    Completed Task - 18

-----------------------------------------------------------------------------------------------------------------------------














