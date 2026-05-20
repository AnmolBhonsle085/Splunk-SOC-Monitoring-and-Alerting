**Splunk Web Log Monitoring**

**Project Overview**

This project demonstrates basic web log monitoring and alert creation using Splunk Enterprise. The project focuses on analyzing web server access logs, searching important events using SPL queries, and creating alerts for monitoring activities such as purchase actions.

The logs used in this project are sample practice logs used for learning and educational purposes only.

**Objectives**

Learn basic SIEM operations using Splunk
Monitor and analyze web server logs
Search events using SPL queries
Detect purchase-related activities
Create automated alerts in Splunk
Understand scheduled and real-time alerting
Tools & Technologies Used
Splunk Enterprise
SPL (Search Processing Language)
Windows 11
Sample Web Access Logs

**SPL Query Used**

index=main "purchase" source="access_30DAY.log" sourcetype="access_combined_wcookie" | sort - count

Query Explanation
index=main → Searches logs stored in the main index
"purchase" → Finds events containing the word purchase
source="access_30DAY.log" → Uses the specified log file
sourcetype="access_combined_wcookie" → Filters logs by sourcetype
sort - count → Sorts results in descending order

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

Search Query Screenshot
Alert Creation Screenshot
Search Results Screenshot

**Learning Outcome**

**This project helped in understanding:**

How SIEM tools work
Basic SOC analyst operations
Log analysis techniques
Alert configuration in Splunk
Monitoring suspicious or important activities

**Note**

The logs used in this project are sample logs used only for practice and educational purposes.
