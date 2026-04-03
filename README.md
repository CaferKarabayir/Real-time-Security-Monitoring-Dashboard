
<img width="1831" height="432" alt="Dashboard Preview" src="https://github.com/user-attachments/assets/89e7c71f-311c-4c4b-9c8b-b9b1f9490fb9" />



GitHub repuna bu başlıklarla girmen, senin SPL (Splunk Search Processing Language) ve Security Visualization becerini parlatır.
🚀 Splunk Live Attack Monitoring Dashboard

This repository showcases a professional Security Monitoring Dashboard built in Splunk to detect and visualize real-time brute-force attacks and authentication failures.
📊 Overview

The goal of this dashboard is to provide immediate visibility into security events by monitoring system authentication logs. It transforms raw log data into an actionable visual timeline, allowing analysts to identify attack patterns as they happen.
🔍 The Search Logic (SPL)

To power the dashboard, I developed a custom SPL (Search Processing Language) query that specifically targets failed login attempts.

Query:
source="/host_logs/auth.log" ("authentication failure" OR "incorrect password") 
| timechart span=1m count

How it works:

    Filtering: The search scans the auth.log for specific error strings (authentication failure or incorrect password) used by the Linux OS.

    Aggregation: Using the timechart command, the data is binned into 1-minute intervals.

    Real-time Visualization: This allows the dashboard to display "spikes" in the graph, which are clear indicators of a brute-force or credential stuffing attack.

Gemini said

Tamamdır kanka, gereksiz her şeyi ayıkladım. Sadece "Splunk Dashboard" odaklı, aramanın mantığını ve canlı izleme (live monitoring) kısmını ön plana çıkaran, çok daha "temiz" bir İngilizce metin hazırladım.

GitHub repuna bu başlıklarla girmen, senin SPL (Splunk Search Processing Language) ve Security Visualization becerini parlatır.
🚀 Splunk Live Attack Monitoring Dashboard

This repository showcases a professional Security Monitoring Dashboard built in Splunk to detect and visualize real-time brute-force attacks and authentication failures.
📊 Overview

The goal of this dashboard is to provide immediate visibility into security events by monitoring system authentication logs. It transforms raw log data into an actionable visual timeline, allowing analysts to identify attack patterns as they happen.
🔍 The Search Logic (SPL)

To power the dashboard, I developed a custom SPL (Search Processing Language) query that specifically targets failed login attempts.

Query:
Splunk SPL

source="/host_logs/auth.log" ("authentication failure" OR "incorrect password") 
| timechart span=1m count

How it works:

    Filtering: The search scans the auth.log for specific error strings (authentication failure or incorrect password) used by the Linux OS.

    Aggregation: Using the timechart command, the data is binned into 1-minute intervals.

    Real-time Visualization: This allows the dashboard to display "spikes" in the graph, which are clear indicators of a brute-force or credential stuffing attack.

📈 Dashboard Features

    Live Attack Timeline: A dynamic line/column chart that updates in real-time.

    Granular Monitoring: Captured specific failure events that standard "invalid user" queries might miss due to OS-specific log formatting.

    Incident Detection: Designed to alert security teams when the count of failures exceeds normal baseline thresholds within a short window.

💡 Technical Takeaways

    Event Identification: Successfully identified the correct log patterns (authentication failure) by analyzing raw system logs.

    Visual Analytics: Leveraged Splunk’s visualization engine to convert text-based logs into high-impact security metrics.

    Latency-Free Monitoring: Configured the dashboard for real-time search mode to ensure zero-delay visibility.
