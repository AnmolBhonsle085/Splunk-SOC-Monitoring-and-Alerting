**Splunk Web Log Monitoring**

**Project Overview**

This project demonstrates basic web log monitoring and alert creation using Splunk Enterprise. The project focuses on analyzing web server access logs, searching important events using SPL queries, and creating alerts for monitoring activities such as purchase actions.

The logs used in this project are sample practice logs used for learning and educational purposes only.

**Objectives**

Learn basic SIEM operations using Splunk Enterprise.
Analyze Apache web server access logs using SPL queries.
Search and investigate web activity based on client IP, HTTP method, URI, and status code.
Search for specific web activity, such as purchase-related events, from a particular client IP.
Create alerts for selected log events.

**Tools & Technologies**

- Splunk Enterprise
- SPL (Search Processing Language)
- Apache Web Server Access Logs
- Windows 11
- Sample Web Access Logs

**SPL Query Used**

1) index=main "purchase" source="access_30DAY.log" sourcetype="access_combined_wcookie" | sort - count

- Searches the Apache web server logs for purchase-related events using the specified source and sourcetype.
   
3) index="main" source="access_30day.log" clientip="87.240.128.18" "purchase"

- Used to search for purchase-related events associated with a specific client IP address.

4) index="main" source="access_30day.log"
| table _time clientip method status uri

- Used to display key information from web-server events: Timestamp, Client IP, HTTP method, HTTP status code, Requested URI

**Alert Configuration**

The search query was saved as an alert in Splunk.

Alert Details
Alert Type: Scheduled
Trigger Condition: Number of results greater than 0
Purpose: Detect purchase-related activities automatically

**Features**

Web log monitoring
Event searching
SPL query analysis
Alert creation
Security monitoring basics

**Screenshots**

- Search Query Screenshots
- Alert Creation Screenshot
- Search Results Screenshot
- Report
  
**Learning Outcome**

**This project helped in understanding:**

How SIEM tools work
Basic SOC analyst operations
SPL Queries
Log analysis techniques
Alert configuration in Splunk
Monitoring suspicious or important activities

**Note**

The logs used in this project are sample logs used only for practice and educational purposes.
