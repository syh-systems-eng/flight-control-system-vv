# System Test Cases

This document defines initial system-level test cases for the Simplified Flight Control System — Altitude Hold Function.

## TC-001 — Accept valid target altitude

| Field | Details |
|---|---|
| Requirement(s) | FCS-REQ-001 |
| Objective | Verify that the system accepts a valid target altitude. |
| Preconditions | System is in Normal mode. |
| Input | Target altitude = 10,000 ft |
| Expected Result | Target altitude is accepted for processing. |
| Verification Method | Test |
| Status | Not Run |

## TC-002 — Reject invalid current altitude

| Field | Details |
|---|---|
| Requirement(s) | FCS-REQ-002, FCS-REQ-006, FCS-REQ-007 |
| Objective | Verify that invalid altitude data is detected and warning status is set. |
| Preconditions | System is powered and ready to process inputs. |
| Input | Current altitude = 45,000 ft |
| Expected Result | Input is identified as invalid and warning flag is set to True. |
| Verification Method | Test |
| Status | Not Run |

## TC-003 — Calculate altitude error

| Field | Details |
|---|---|
| Requirement(s) | FCS-REQ-003 |
| Objective | Verify that altitude error is calculated correctly. |
| Preconditions | Valid target altitude and current altitude are available. |
| Input | Target altitude = 10,000 ft; Current altitude = 8,000 ft |
| Expected Result | Altitude error = +2,000 ft |
| Verification Method | Test |
| Status | Not Run |

## TC-004 — Generate climb pitch command

| Field | Details |
|---|---|
| Requirement(s) | FCS-REQ-004 |
| Objective | Verify that the system commands nose-up pitch when below target altitude. |
| Preconditions | System is in Normal mode with valid input data. |
| Input | Target altitude = 10,000 ft; Current altitude = 8,000 ft |
| Expected Result | Pitch command is positive. |
| Verification Method | Test |
| Status | Not Run |

## TC-005 — Limit pitch command

| Field | Details |
|---|---|
| Requirement(s) | FCS-REQ-005 |
| Objective | Verify that pitch command does not exceed the defined safety limit. |
| Preconditions | System is in Normal mode. |
| Input | Large positive altitude error |
| Expected Result | Pitch command is limited to no more than +15 degrees. |
| Verification Method | Test |
| Status | Not Run |
