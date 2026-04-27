# Test Report — Simplified Flight Control System

## 1. Purpose

This report summarises the results of system-level testing performed on the Simplified Flight Control System — Altitude Hold Function.

The objective is to verify that the system meets defined requirements and behaves correctly under normal and fault conditions.

---

## 2. Test Scope

The following areas were tested:

- Input validation
- Altitude control logic
- Pitch command generation
- Safety constraints
- Fault handling (Degraded and Fail-safe modes)

---

## 3. Test Environment

- Test Type: Simulation (Python-based logic)
- Platform: Local execution / conceptual validation
- Limitations: No real aircraft dynamics or hardware integration

---

## 4. Test Summary

| Test Case ID | Description | Result |
|---|---|---|
| TC-001 | Accept valid target altitude | Pass |
| TC-002 | Reject invalid altitude input | Pass |
| TC-003 | Calculate altitude error | Pass |
| TC-004 | Generate climb pitch command | Pass |
| TC-005 | Limit pitch command | Pass |
| TC-006 | Enter Degraded mode | Pass |
| TC-007 | Enter Fail-safe mode | Pass |
| TC-008 | Neutral pitch in Fail-safe | Pass |

---

## 5. Defects Identified

| Defect ID | Description | Severity | Status |
|---|---|---|---|
| DEF-001 | Warning flag not triggered for airspeed failure in early version | Medium | Fixed |
| DEF-002 | Pitch command briefly exceeded limit before constraint applied | High | Fixed |

---

## 6. Requirement Coverage

All defined system requirements (FCS-REQ-001 to FCS-REQ-010) were verified through corresponding test cases.

---

## 7. Conclusion

The system successfully meets the defined functional and safety requirements under the tested conditions.

The system demonstrates correct behaviour for:

- altitude tracking logic
- safety constraint enforcement
- degraded operation
- fail-safe response

Further work may include:

- more detailed control dynamics
- additional sensor validation scenarios
- performance testing

---

## 8. Notes

This project is a simplified simulation intended to demonstrate system-level Verification & Validation practices rather than real aircraft system behaviour.
