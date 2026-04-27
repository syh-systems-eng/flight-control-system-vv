# Requirements Traceability Matrix

This matrix maps system requirements to corresponding test cases to ensure full verification coverage.

| Requirement ID | Requirement Description | Test Case ID(s) | Verification Status |
|---|---|---|---|
| FCS-REQ-001 | Accept target altitude input | TC-001 | Not Verified |
| FCS-REQ-002 | Validate current altitude input | TC-002 | Not Verified |
| FCS-REQ-003 | Calculate altitude error | TC-003 | Not Verified |
| FCS-REQ-004 | Generate pitch command based on altitude error | TC-004 | Not Verified |
| FCS-REQ-005 | Limit pitch command range | TC-005 | Not Verified |
| FCS-REQ-006 | Detect invalid altitude input | TC-002 | Not Verified |
| FCS-REQ-007 | Set warning flag for invalid input | TC-002, TC-006, TC-007 | Not Verified |
| FCS-REQ-008 | Enter Degraded mode for non-critical failure | TC-006 | Not Verified |
| FCS-REQ-009 | Enter Fail-safe mode for critical failure | TC-007 | Not Verified |
| FCS-REQ-010 | Command neutral pitch in Fail-safe mode | TC-008 | Not Verified |
| FCS-REQ-011 | Maintain stable pitch under fluctuating valid altitude input | TC-009 | Not Verified |
| FCS-REQ-012 | Detect unstable or inconsistent altitude input data | TC-010 | Not Verified |
