# Google Dorking – Information Gathering & OSINT Security Assessment

A passive Google Dorking / OSINT reconnaissance project. This repo documents the methodology, findings, evidence, and remediation recommendations for publicly indexed information discovered through search-engine reconnaissance — no authentication, exploitation, or unauthorized access was performed against any target.

📄 **[Read the full report]([https://github.com/amaresh-javali/google-dorking-information-gathering/blob/main/Google-Dork-OSINT-Security-Assessment-Report.pdf])**

## Overview

- **Assessment type:** Passive Google Dork / OSINT reconnaissance
- **Scope:** Publicly indexed assets identified via passive search-engine reconnaissance
- **Total observations:** 10
  - 5 confirmed technical vulnerabilities
  - 5 informational / reconnaissance-value observations
- **Highest-severity findings:** unauthenticated live camera feed, publicly exposed `.env` file with database credentials

## What's in this repo

| File | Description |
|---|---|
| `Google-Dork-OSINT-Security-Assessment-Report.pdf` | Full security assessment report (findings, evidence, remediation) |
| `README.md` | Project overview |

## Methodology

All findings were identified using **passive reconnaissance only**:

- Google Dorks were used to filter publicly indexed content into categories of interest (exposed directories, configuration files, login portals, etc.)
- Every result was manually reviewed in a browser to confirm it was genuinely reachable and to capture evidence
- No credentials were entered, guessed, or reused
- No files were downloaded or analyzed beyond what a browser already renders
- No scanning, brute-forcing, exploitation, or denial-of-service activity was performed

Each finding separates what was directly **Observed**, what was **Demonstrated** during testing, and what remains a **Potential** (unverified) impact — so severity ratings aren't inflated beyond what the evidence supports.

## Findings Summary

| ID | Finding | Type |
|---|---|---|
| F-01 | Exposed Backend Source Code Directory | Vulnerability |
| F-02 | Publicly Accessible Git Repository (`.git`) | Vulnerability |
| F-03 | Unauthenticated Live Camera Feed | Vulnerability |
| F-04 | Exposed `.env` File Containing Database Credentials | Vulnerability |
| F-05 | Potentially Sensitive Password-Related Files in a Public Directory | Vulnerability |
| F-06 | Publicly Indexed Administrative Login Page | Informational |
| F-07 | Information Disclosure via `robots.txt` | Informational |
| F-08 | Public Plans Directory Listing | Informational |
| F-09 | Publicly Indexed Subdomains and Login Portals | Informational |
| F-10 | Publicly Accessible Corporate Financial Document | Informational |

Full detail, evidence, and remediation guidance for every finding is in the report.

## Disclosure

Where a finding references a specific organization or domain, this project does not assert formal authorization from that organization — targets were chosen as illustrative, real-world examples of exposure discoverable through passive reconnaissance. Responsible disclosure messages for each affected party are included in the report.

## Disclaimer

This project is for educational and research purposes only. All testing was passive and non-intrusive. Anyone acting on these findings should confirm their own authorization before taking action on systems they do not own or operate.
