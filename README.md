# Flight Control System V&V Portfolio Project

## Overview

This project demonstrates system-level Verification & Validation (V&V) for a simplified Flight Control System, focusing on an Altitude Hold Control Function inspired by commercial aircraft such as the :contentReference[oaicite:0]{index=0}.

The objective is not to simulate full aircraft behaviour, but to showcase systems engineering thinking, including requirements definition, integration behaviour, fault handling, and verification strategy.

---

## Why this project

As a QA Test Engineer transitioning into Systems Integration and V&V roles, I built this project to move beyond feature-level testing and demonstrate:

- system-level thinking  
- requirement-driven development  
- verification planning and traceability  
- fault handling and safety behaviour  

---

## System Under Test

A simplified **Altitude Hold Control Function** that:

### Inputs
- Target altitude (0 – 40,000 ft)
- Current altitude
- Vertical speed
- Airspeed
- Sensor validity flags

### Outputs
- Pitch command (-15° to +15°)
- Thrust command (0–100%)
- System mode (Normal / Degraded / Fail-safe)
- Warning flag

---

## Key Features

- Defined system boundary and assumptions  
- Developed formal system requirements (“The system shall…”)  
- Designed system-level test cases covering:
  - nominal behaviour  
  - boundary conditions  
  - fault scenarios  
- Implemented fault handling:
  - Degraded mode  
  - Fail-safe mode  
- Built a full requirements traceability matrix  
- Produced a structured test report including defect identification

---

## V&V Artefacts

| Artefact | Description |
|---|---|
| [System Overview](docs/01_system_overview.md) | Defines system boundary, inputs, outputs and assumptions |
| [System Requirements](requirements/system_requirements.md) | Formal functional and safety requirements |
| [Test Cases](tests/test_cases.md) | System-level verification scenarios |
| [Traceability Matrix](requirements/traceability_matrix.md) | Requirement-to-test mapping |
| [Test Report](docs/07_test_report.md) | Test results, defects and conclusions |

---

## Example Scenario

**Fail-safe behaviour:**

When critical sensor data (e.g. altitude) becomes invalid:

- The system enters Fail-safe mode  
- A warning flag is raised  
- Pitch command defaults to 0°  

This ensures safe system behaviour under failure conditions.

---

## Tools & Approach

- Documentation: Markdown (GitHub)
- Test Design: System-level V&V methodology
- Approach: Requirement-driven verification with traceability

---

## What this demonstrates

This project reflects key skills required for Systems Integration and V&V roles:

- translating system behaviour into testable requirements  
- designing scenario-based system tests  
- handling degraded and failure modes  
- maintaining requirement-to-test traceability  
- producing structured verification evidence  

---

## Future Improvements

- Extend control logic realism (non-linear response)
- Add additional sensor failure scenarios
- Introduce timing/performance requirements
- Implement a lightweight simulation model in Python
- Introduce environmental disturbance scenarios (e.g. turbulence, wind gusts) by simulating unstable or rapidly changing input data
- Evaluate system robustness under fluctuating altitude and vertical speed conditions
- Extend fault handling to cover sensor noise and inconsistent data caused by environmental effects

---

## Notes

This is a simplified portfolio project designed to demonstrate systems engineering and V&V practices, not to replicate real aircraft flight control systems.
