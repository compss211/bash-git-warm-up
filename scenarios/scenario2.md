# Scenario 2: Web Server Log Analysis

## The Problem

You're studying online community behavior by analyzing web server logs from a research forum. The logs contain information about user visits, page views, and download patterns that could reveal insights about how people engage with academic content.

## Your Task

Write a bash script that analyzes web server log files to extract meaningful statistics for social science research.

## Sample Log Format
```
127.0.0.1 - - [10/Jan/2024:13:55:36 +0000] "GET /research/papers/social-networks.pdf HTTP/1.1" 200 2326
192.168.1.15 - - [10/Jan/2024:13:55:37 +0000] "GET /forum/discussion/thread123 HTTP/1.1" 200 1543
10.0.0.1 - - [10/Jan/2024:14:02:15 +0000] "POST /forum/login HTTP/1.1" 200 856
127.0.0.1 - - [10/Jan/2024:14:05:22 +0000] "GET /research/papers/nlp-analysis.pdf HTTP/1.1" 404 324
192.168.1.20 - - [10/Jan/2024:14:12:44 +0000] "GET /forum/discussion/thread456 HTTP/1.1" 200 2100
```

## Requirements

Your script should analyze the log file and generate a report with:

1. **Basic Statistics:**
   - Total number of requests
   - Number of unique IP addresses (unique visitors)
   - Date range of the logs
   - Number of successful requests (200 status) vs errors (404, 500, etc.)

2. **Content Analysis:**
   - Most popular research papers (PDF downloads)
   - Most accessed forum discussions
   - Peak activity hours (when do people visit most?)

3. **User Behavior Patterns:**
   - Top 5 most active IP addresses
   - Average requests per visitor
   - Most common request types (GET, POST, etc.)

4. **Research-Relevant Insights:**
   - Which research topics are most popular? (extract from PDF filenames)
   - Forum engagement metrics (discussion thread views)
   - Error rate analysis (what content is missing?)

## Sample Output Format
```
=== WEB SERVER LOG ANALYSIS REPORT ===
Analysis Date: 2024-01-15
Log File: server_access.log

BASIC STATISTICS:
- Total Requests: 1,245
- Unique Visitors: 89
- Date Range: Jan 10 - Jan 15, 2024
- Success Rate: 92.3% (1,149/1,245 successful)

POPULAR CONTENT:
Top Research Papers:
1. social-networks.pdf (45 downloads)
2. nlp-analysis.pdf (32 downloads)
3. data-mining.pdf (28 downloads)

Peak Activity: 2:00 PM - 3:00 PM (EST)

RESEARCH INSIGHTS:
- Most interest in: social network analysis
- Forum activity: 234 discussion views
- Error rate: 7.7% (mostly missing papers)
```

## Test Your Script

Create a sample log file with various entries to test your script. You can use the sample format above and add more entries.

## Bonus Challenge (Optional)

- Detect potential bot traffic (same IP making many rapid requests)
- Geographic analysis if you can map IP ranges to regions
- Time-series analysis showing activity patterns over days

## Real-World Application

Log analysis is crucial for understanding online behavior patterns, content popularity, and user engagement in digital humanities and computational social science research.