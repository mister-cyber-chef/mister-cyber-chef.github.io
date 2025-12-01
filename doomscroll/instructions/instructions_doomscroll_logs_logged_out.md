# Instructions

---

# Prerequisites
- Download the `doomscroll_logs_logged_out.db.zip` by navigating to `https://mister-cyber-chef.github.io/doomscroll/db_assets/doomscroll_logs_logged_out.db.zip` or directly from github at `https://github.com/mister-cyber-chef/mister-cyber-chef.github.io/tree/main/doomscroll/db_assets`
- Unzip `doomscroll_logs_logged_out.db.zip`
- Upload the `doomscroll_logs_logged_out.db` file to `https://mister-cyber-chef.github.io/doomscroll/doomscroll_ctf.html`
  
## Scenario

Yesterday, the DoomScroll security team observed **unusual patterns** in a batch of **logged out web traffic** hitting the primary site:

`web.doomscroll.net`

To investigate, you’ve been given a **single day of HTTP logs** (~300,000 rows) captured during the period of interest.

---

## Your Goal

Determine whether **automated scraping** is occurring and, if so:

Identify and Understand **which clients** are responsible and **what they are doing / targeting**   

**Your task is to:**

- Discover patterns in the traffic
- Isolate suspicious behavior
- Aarrive at a **defensible conclusion** and justify your findings using SQL queries

---

## You May Assume

- Logs represent a mix of **normal** and **potentially automated** traffic  
- Suspicious activity is **not labeled**  
- All traffic is **logged out**

---

## The Dataset

You’ll be working with a **SQLite database**:

- **Database:** `doomscroll_ctf_logged_out.db`
- **Table:** `doomscroll_logs_logged_out`

All rows represent **logged out** requests only.

### Table Fields

- `timestamp`  
- `uri`  
- `userID`  
- `IP`  
- `ASN`  
- `requestHeaders`  
- `requestCookieNames`  
- `JA4`  
- `userAgent`  
- `parameters`  
- `responseCode`  
- `responseContentSize`  
- `endpointKey`  
- `authStatus`  
- `serverLocal`  

### Important Notes

- `authStatus` will always be `"logged_out"` with `userID` equaling `"0"`   
- **IPs are intentionally non routable for safety.**
