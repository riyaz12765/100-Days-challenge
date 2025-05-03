# 🧪 Lab Title: Splunk Basics – DNS Log Analysis

---

## 🎯 Objective

In this lab, you will:
- Learn how to ingest and analyze DNS logs in Splunk.
- Understand how to extract useful information such as DNS query types, source hosts, and common destinations.
- Practice building basic SPL (Search Processing Language) queries to investigate DNS activity.

---

## 🖥️ Lab Setup

- ✅ **Splunk**: Already installed and accessible.
- ✅ **Data Source**: JSON-formatted Zeek DNS logs.
- 🌐 **Log File**: Download the file below and place it in a directory accessible to Splunk for ingestion.

📥 **[Download sample dns file](https://raw.githubusercontent.com/0xrajneesh/30-Days-SOC-Challenge-Beginner/refs/heads/main/dns_logs.json)**

---

## ⚙️ Steps to Upload DNS Log into Splunk

1. Go to Splunk Web → **Settings > Add Data**.
2. Choose **Upload** and select the file `dns.log`.
3. Set Source type: `json` or create a custom source type `dns`.
4. Index: Choose `main` or create a new index like `dns_lab`.
5. Finish the upload and confirm indexing.

---

## 🔍 Lab Tasks

Use SPL queries to answer the following:

### ✅Task 1: Identify the most frequently queried domain names

### ✅Task 2: Find the most active user IPs generating DNS traffic

### ✅Task 3: Breakdown of DNS query types (A, AAAA, CNAME, PTR)

## 📸Submission
Submit a screenshot of each of the following:
- Your SPL query and result for Task 1.
- SPL query and result for Task 2.
- SPL query and result for Task 3.



-----------------------------------------------------------------------------------------------------------------------------------

### Output of Task - 17
------------------------

* In this task am just learn how to upload dns.log file into the splunk and how to analyze, Investigation.
* Also learn some spl splunk queries its reall help for soc analyst.


Task 1: Identify the most frequently queried domain names
---------------------------------------------------
![Screenshot 2025-05-03 115535](https://github.com/user-attachments/assets/b783b2e3-7f55-45d0-b2a5-f28599402c3f)


Task 2: Find the most active user IPs generating DNS traffic
--------------------------------------------------------------

![Screenshot 2025-05-03 115654](https://github.com/user-attachments/assets/3ed63a7f-5437-4afb-8bd7-afa0591d9b80)


Task 3: Breakdown of DNS query types (A, AAAA, CNAME, PTR)
---------------------------------------------------------------

![Screenshot 2025-05-03 121333](https://github.com/user-attachments/assets/1a4f17ba-69b2-4b3a-92e3-654df1c8c5dc)

--------------------------------------------------------------------------------------------------------------------------------
   Completed Task - 17

-----------------------------------------------------------------------------------------------------


















