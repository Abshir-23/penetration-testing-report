# Penetration Testing Report

A full web application and infrastructure penetration test, written up as a professional vulnerability assessment report.

## Overview

The assignment was to assess a vulnerable web application and its underlying Linux server, then document everything the way a real security consultancy would deliver it to a client. The engagement was run as a whitebox test following the **OWASP Web Security Testing Guide v4.2**, covering both the application layer and the host.

**38 vulnerabilities** were identified and classified on the CVSS v3 scale:

| Severity | Count | Examples |
|----------|-------|----------|
| 🔴 **Critical** | 5 | Stored & Reflected XSS, SQL Injection, IDOR, broken access control |
| 🟠 **High** | 18 | Path Traversal, privilege escalation (CVE-2021-4034, CVE-2021-3156), weak password hashing, outdated services |
| 🟡 **Medium** | 7 | Missing anti-CSRF tokens, missing security headers, weak authentication |
| 🟢 **Low** | 7 | Cookie flag issues, information disclosure in headers |
| ⚪ **Informational** | 6 | Cache-control misconfiguration, sensitive info in URLs |

## What the report covers

- **Methodology** – scope, rules of engagement, access, and a documented testing process based on OWASP WSTG 4.2
- **Classification** – each finding scored with CVSS v3 and grouped by severity
- **Findings** – for every vulnerability: observation, affected area, description, impact, mitigation, and validation
- **Remediation advice** – concrete, prioritised recommendations for the client

## Tools used

Nmap · OWASP ZAP · Nikto · Tenable Nessus · Wireshark · Metasploit · SQLmap · John the Ripper · Hashcat · Hydra · Snyk

## What I took from it

Writing this taught me how to turn raw technical findings into something a client can actually act on: clear severity ratings, a consistent structure per finding, and mitigation advice tied to the risk. It also gave me hands-on familiarity with the OWASP WSTG methodology end to end.

> The full report was written for a lab environment with an authorised, vulnerable target. No real systems were tested.
