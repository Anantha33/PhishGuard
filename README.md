# PhishGuard

## Problem Statement

### Problem:
Phishing attacks continue to be one of the most common and effective cyber threats worldwide. Many users lack the technical knowledge to identify malicious URLs or spoofed emails, and small organizations often do not have affordable tools to analyze suspicious content.

### Solution:
PhishGuard is a web-based application that allows users to analyze suspicious URLs and email headers to identify potential phishing attempts, while also educating users on why the content is dangerous.

---

## Functional Requirements

- FR-1:	  User can submit a URL for phishing analysis
- FR-2:	  User can submit email headers for analysis
- FR-3:	  System returns a risk score and verdict
- FR-4:	  System explains why content is risky
- FR-5:	  User can report phishing attempts

## Non-Functional Requirements:

- NFR-1:	  Fast API response (< 2 seconds for basic checks)
- NFR-2:  Secure input handling (no injection vulnerabilities)
- NFR-3:	  Scalable API design
- NFR-4:  Easy-to-understand UI

---

## Assumptions:

- Users may not have technical knowledge
- Input may be malicious or malformed
- Initial version does not rely on ML

## Constraints:

- Built using Python
- Free/open-source tools only
- Deployed on low-cost or free cloud services

---

## System Design:

User → Web UI → Backend API → Analysis Engine → Risk Score → UI

---

## Threat Modeling:

Threat and Mitigation

- SQL:             Injection	Input validation & parameterized queries
- XSS:	            Output encoding
- Malicious:       Input	Strict input length checks
- Abuse of API:	  Rate limiting (future)
