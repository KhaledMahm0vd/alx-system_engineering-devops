# Postmortem:
Issue Summary:

The outage occurred on August 12, 2024, from 2:15 PM to 4:45 PM UTC, lasting a total of 2 hours and 30 minutes.  The root cause of the issue was a memory leak in the web application server, leading to resource exhaustion.

Timeline:

2:15 PM UTC: Issue detected through an automated monitoring alert indicating high response times on the web application.
2:20 PM UTC: Initial investigation began by the on-call engineer, focusing on database performance, suspecting a slow query.
2:45 PM UTC: The issue was escalated to the backend development team as CPU usage spiked.
3:00 PM UTC: The backend team began investigating recent code deployments and potential bugs in the application code.
3:20 PM UTC: A memory leak was identified in the latest release of the web application.
3:30 PM UTC: Misleading debugging path: initially thought the issue was related to an external API call.
3:45 PM UTC: Rollback of the latest release was initiated.
4:15 PM UTC: Application servers began stabilizing as memory consumption normalized.
4:30 PM UTC: User experience improved significantly as the rollback completed.
4:45 PM UTC: Monitoring confirmed full recovery, and the incident was declared resolved.
Root Cause and Resolution:

The root cause of the issue was a memory leak introduced in the latest release of our web application. As memory usage increased, the application became slower, eventually resulting in server crashes.

To resolve the issue, the team rolled back to the previous stable release, which did not contain the memory leak. Once the rollback was completed, server memory consumption returned to normal levels, and the platform's performance improved.

Corrective and Preventative Measures:

Improvements:

Implement additional monitoring on application memory usage to catch similar issues earlier.

Tasks:

 Patch the memory leak issue in the development branch and deploy it after rigorous testing.
 Add memory usage alerts to the monitoring system with thresholds for early warning.
 Conduct a code review process focused on performance and memory management for all new features.
 Create a runbook for quicker rollbacks during future incidents.
 ![The Great Memory Leak Adventure](/diagram.png)

