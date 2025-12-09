# Instructions

## Scenario

Yesterday, the DoomScroll security team received a report from a partner indicating that **some kind of automated scraping activity** may be occurring against the mobile site:

```
m.doomscroll.net
```

To investigate, you've been handed a **single day of HTTP logs** (~300,000 entries) captured during the suspected activity window.

### Your Goal

Identify the bad actor and determine what they are doing using **SQL**.

You are not being told what endpoint or dataset is being targeted.  

**Your task is to:**

- Discover patterns in the traffic
- Isolate suspicious behavior
- Aarrive at a **defensible conclusion** and justify your findings using SQL queries

**You may assume:**

- Logs represent real user and partner traffic mixed with noise
- Suspicious traffic is present but not labeled

---

## The Dataset

You’ll be working with a SQLite database:

#### Table:

```
doomscroll_logs_logged_in
```

### Table Fields

```
timestamp
uri
userID
IP
ASN
requestHeaders
requestCookieNames
JA4
userAgent
parameters
responseCode
responseContentSize
```