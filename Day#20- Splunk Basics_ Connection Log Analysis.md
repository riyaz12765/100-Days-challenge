# Day#20: Splunk Basics – Zeek Connection Log Analysis

---

## 🎯 Objective

In this lab, you will:

- Learn how to upload and search Zeek connection logs in Splunk.
- Find top clients, top servers, and most common services.
- Identify large traffic and long connections.

---

## 🖥️ Lab Setup

- ✅ **Splunk**: Already installed and accessible.
- ✅ **Data Source**: JSON-formatted Zeek-style connection logs.
- 🌐 **Log File**: Download and upload to Splunk using the steps below.

📥 **[Download Zeek Conn Log File](https://raw.githubusercontent.com/0xrajneesh/30-Days-SOC-Challenge-Beginner/refs/heads/main/zeek_conn_logs.json)**

---

## ⚙️ Steps to Upload Conn Log into Splunk

1. Go to **Splunk Web → Settings > Add Data**.
2. Choose **Upload** and select `zeek_conn_logs.json`.
3. Set **Source type**: `json` or create a new one like `zeek:conn`.
4. Index: Use `main` or create a new one called `conn_lab`.
5. Complete the upload and check that logs are searchable.

---

## 🔍 Lab Tasks

Use the following SPL queries to complete each task:

---

### ✅Task 1: Find the Top 10 Client IPs (id.orig_h)

### ✅Task 2: List Most Common Services

### ✅Task 3: Find Connections with Duration > 1 Second

### ✅Task 4: Identify the Most Accessed Internal Servers


## 📸 Submission
Submit a screenshot for each of the following:
- Your query and result for Task 1.
- Your query and result for Task 2.
- Your query and result for Task 3.
- Your query and result for Task 4.

---------------------------------------------------------------------

###Output of Task - 20
-------------------------

* Zeek is a power network monitoring tool also its open source tool
* configure zeek logs into splunk and analyze for investigation.
* also learn some spl query in splunk for filter zeek logs.

Task 1: Find the Top 10 Client IPs (id.orig_h)
-----------------------------------------------
![Screenshot 2025-05-03 145526](https://github.com/user-attachments/assets/6d8df53b-384f-4a32-9e20-1154f1aa264c)


Task 2: List Most Common Services
------------------------------------
![Screenshot 2025-05-03 145749](https://github.com/user-attachments/assets/25e59bff-fd9f-416f-90c2-3ce594ea091b)


Task 3: Find Connections with Duration > 1 Second
---------------------------------------------------

![Screenshot 2025-05-03 145933](https://github.com/user-attachments/assets/7f3e9d38-e7d3-4ed7-b0bc-41ed371da1d5)


Task 4: Identify the Most Accessed Internal Servers
---------------------------------------------------

![Screenshot 2025-05-03 150229](https://github.com/user-attachments/assets/f1383e2e-1544-430a-9ceb-be0e0a6be3d9)

------------------------------------------------------------------------------------------------------------------

Completed task - 20

---------------------------------------------------------------------------------------------------------------------












