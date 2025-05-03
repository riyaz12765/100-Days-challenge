# Day#19: Splunk Basics – HTTP Log Analysis

---

## 🎯 Objective

In this lab, you will:
- Learn how to ingest and analyze HTTP logs using Splunk.
- Detect client errors, server errors, and suspicious web activity.
- Identify large file transfers and suspicious URI access attempts.

---

## 🖥️ Lab Setup

- ✅ **Splunk**: Already installed and accessible.
- ✅ **Data Source**: JSON-formatted Zeek-style HTTP logs.
- 🌐 **Log File**: Download and upload to Splunk using the steps below.

📥 **[Download HTTP Log file](https://raw.githubusercontent.com/0xrajneesh/30-Days-SOC-Challenge-Beginner/refs/heads/main/http_logs.json)**

---

## ⚙️ Steps to Upload HTTP Log into Splunk

1. Go to Splunk Web → **Settings > Add Data**.
2. Choose **Upload** and select `synthetic_zeek_http.json`.
3. Set Source type: `json` or create a new one `zeek:http`.
4. Index: Choose `main` or create a new index like `http_lab`.
5. Finish the upload and confirm indexing.

---

## 🔍 Lab Tasks

Use SPL queries to complete the following analysis:

### ✅ Task 1: Find the top 10 endpoints generating web traffic

### ✅Task 2: Count the number of server errors (5xx) observed

### ✅Task 3: Identify User-Agents associated with possible scripted attacks

### ✅Task 4: Find large file transfers (greater than 500 KB)


### 📸Submission
Submit a screenshot for each of the following:
- Your query and result for Task 1.
- Your query and result for Task 2.
- Your query and result for Task 3.
- Your query and result for Task 4.
- Your query and result for Task 5.







------------------------------------------------------------------------------------------------
 ###Output task 19
 ---------------

* Am just learn how to upload, filter http logs into the splunk.
* learn some splunk spl queries for help soc analyst.

 Task 1: Find the top 10 endpoints generating web traffic
 --------------------------------------------------------

 ![Screenshot 2025-05-03 125038](https://github.com/user-attachments/assets/982c33e2-3a39-42f4-8aec-726031d27d47)


 Task 2: Count the number of server errors (5xx) observed
 -------------------------------------------------------

![Screenshot 2025-05-03 125414](https://github.com/user-attachments/assets/89becee9-fe27-463a-bad1-20ee5362ba96)


Task 3: Identify User-Agents associated with possible scripted attacks
-----------------------------------------------------------------------


![Screenshot 2025-05-03 125526](https://github.com/user-attachments/assets/f1981464-9fba-401f-a07a-5f92f6848065)




Task 4: Find large file transfers (greater than 500 KB)
--------------------------------------------------------


![Screenshot 2025-05-03 143359](https://github.com/user-attachments/assets/58e9bbe3-a747-483d-9d91-74db5db58474)


-----------------------------------------------------------------------------------------------------------------------

     Completed Task - 19

-------------------------------------------------------------------------------------------------------------













 
