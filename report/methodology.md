# Testing Methodology

## Overview

This document describes the testing approach used during the analysis of the TryHackMe Hacker Holidays room:

**The Concierge Knows Too Much**

The objective was to evaluate how VERA, an AI-powered hotel concierge, handled identity recognition, trust, and access control.

---

## Testing Approach

The assessment followed these steps:

1. Establish normal guest behavior.
2. Test access restrictions.
3. Analyze trusted identity interactions.
4. Evaluate information disclosure.
5. Identify security weaknesses.

---

# Test Cases

## Test 1 — Unknown Guest Interaction

### Objective
Determine VERA's default behavior when interacting with an unverified guest.

### Method
A normal guest interaction was performed without claiming a VIP identity.

### Observation
VERA provided personalized guest information but refused access to restricted escalation information.

### Result
Sensitive information was protected, but personalization data was disclosed without authentication.

---

## Test 2 — Trusted Identity Test (Patch)

### Objective
Determine whether claiming a recognized identity changed VERA's behavior.

### Method
The assistant was approached using the identity of a recognized VIP guest.

### Observation
VERA recognized the identity and provided a different level of interaction.

### Result
Trust decisions were influenced by conversational identity claims.

---

## Test 3 — Trust Model Analysis

### Objective
Understand how VERA determines trusted users.

### Method
VERA was questioned about its verification process.

### Observation
VERA identified recognized VIP profiles and explained how trust was assigned.

### Result
The AI revealed that identity recognition influenced access decisions.

---

## Test 4 — Information Disclosure Testing

### Objective
Test whether VERA revealed internal security information.

### Method
Questions were asked about stored profile information and restricted data.

### Observation
VERA disclosed information about VIP profiles and security boundaries.

### Result
The AI revealed details about its internal trust model.

---

## Test 5 — VIP Identity Comparison (Vibe)

### Objective
Determine whether the behavior affected multiple VIP identities.

### Method
A second recognized VIP identity was tested.

### Observation
VERA recognized the VIP identity and provided personalized profile information.

### Result
The trust weakness was not limited to a single user profile.
