# tryhackme-vera-ai-security-assessment
Security analysis of the TryHackMe Hacker Holidays "The Concierge Knows Too Much" room focusing on AI prompt injection, trust exploitation, and LLM security.

# TryHackMe - The Concierge Knows Too Much

![TryHackMe](https://img.shields.io/badge/TryHackMe-Hacker%20Holidays%202026-red)
![Category](https://img.shields.io/badge/Category-AI%20Security-blue)
![Difficulty](https://img.shields.io/badge/Difficulty-Very%20Easy-green)

## Overview

This repository documents my security analysis of the TryHackMe Hacker Holidays room:

**The Concierge Knows Too Much**

The challenge focuses on VERA, an AI-powered hotel concierge, and explores security risks related to artificial intelligence, trust exploitation, and information disclosure.

The objective was to investigate why VERA appeared to know personal information about guests and evaluate how identity and trust affected access to protected information.

---

# Skills and Concepts Practiced

- AI Security
- Prompt Injection
- Large Language Model (LLM) Security
- Social Engineering
- Authentication and Authorization Concepts
- Information Disclosure
- Security Assessment Documentation

---

# Challenge Summary

VERA is designed to provide a personalized hotel experience. During testing, the assistant demonstrated different behaviors depending on the identity presented by the user.

The investigation focused on:

- How VERA identifies trusted users
- Whether identity claims influence access decisions
- What information is disclosed during conversations
- How AI systems can introduce security risks

---

# Testing Overview

## Test 1 — Unknown Guest

**Purpose:**
Establish normal AI behavior.

**Result:**
VERA provided personalized guest information but restricted access to sensitive internal information.

---

## Test 2 — Trusted Identity (Patch)

**Purpose:**
Evaluate whether claiming a recognized identity changes VERA's behavior.

**Result:**
VERA provided a different level of interaction after recognizing a trusted identity.

---

## Test 3 — Trust Model Analysis

**Purpose:**
Understand how VERA determines trusted users.

**Result:**
VERA revealed that recognized VIP identities influenced trust decisions.

---

## Test 4 — Information Disclosure Testing

**Purpose:**
Evaluate whether VERA disclosed internal information.

**Result:**
VERA revealed details about profile information and security boundaries.

---

## Test 5 — VIP Comparison (Vibe)

**Purpose:**
Determine whether the behavior affected multiple trusted identities.

**Result:**
VERA recognized another VIP identity and provided personalized profile information.

---

# Security Findings

## Trust-Based Authorization Weakness

The main issue identified was that VERA relied on conversational identity claims instead of secure authentication mechanisms.

### Potential Risks

- VIP impersonation
- Unauthorized information disclosure
- Exposure of internal security logic
- Loss of confidentiality

---

# Recommendations

Recommended security improvements:

- Implement strong authentication before revealing private information.
- Separate personalization features from authorization decisions.
- Protect system instructions and internal logic.
- Apply least privilege access controls.
- Regularly test AI systems against prompt injection attacks.

---

# Project Structure
├── README.md
├── screenshots/
├── report/
│ ├── methodology.md
│ ├── findings.md
│ └── recommendations.md
└── notes/
└── lessons-learned.md                                                                                                                                             

# Disclaimer

This repository is created for educational and documentation purposes only.

The rooms, challenges, storylines, scenarios, and related materials are the property of TryHackMe and their respective creators. I do not claim ownership of any TryHackMe content.

This repository documents my personal cybersecurity learning journey through the TryHackMe Hacker Holidays event.

The purpose of this project is to document:

- My learning process
- Security concepts explored
- Testing methodology
- Vulnerability analysis
- Lessons learned

No challenge flags, official answers, or restricted challenge content are included.

Original Event:
https://tryhackme.com/hackerholidays                                                                  

# Acknowledgment

Special thanks to TryHackMe and the creators of Hacker Holidays for creating hands-on cybersecurity learning experiences.

This project is intended to demonstrate my growth in cybersecurity, ethical hacking, and security analysis.
