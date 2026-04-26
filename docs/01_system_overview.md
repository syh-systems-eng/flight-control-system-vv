</> Markdown
# System Overview Document
## 1. Project Title
Simplified Flight Control System - Altitude Hold Function
## 2. Objective
The objective of this project is to define and verify a simplified flight control function that maintains a commanded target altitude. This project is intended to demonstrate system-level Verification & Validation thinking, including requirements definition, system boundary analysis, input/output definition, fault handling and test planning.
## 3. Real-World Reference
This project uses a commercial passenger aircraft, similar to the Airbus A320, as a high-level reference. The project does not attempt to model the real Airbus A320 flight control system. Instead, it uses simplified and representative values to demonstrate systems engineering and V&V practices.
## 4. System Under Test
The System Under Test is the Altitude Hold Control Function.
The function receives:
-target altitude
-current altitude
-current vertical speed
-current airspeed
-sensor validity status
The function outputs:
-pitch command
-thrust command
-system mode
-warning status
## 5. System Boundary
### Inside the system boundary
The following are included:
-Input validation
-Altitude error calculation
-Pitch command calculation
-Thrust command calculation
-Mode selection logic
-Fault handling logic
-Warning generation
### Outside the system boundary
The following are excluded:
-Real aircraft aerodynamics
-Full aircraft simulation
-Weather effects
-Pilot behaviour modelling
-Real Airbus A320 flight control laws
-Hardware-in-the-loop testing
-Certification-level compliance
## 6. Operating Modes
The system has three operating modes:
| Mode | Description |
|---|---|
| Normal | All required inputs are valid and the system can calculate pitch and thrust commands |
| Degraded | One non-critical input is invalid, but the system can continue operating with limitations |
| Fail-safe | Critical input data is invalid and the system commands safe default outputs |

## 7. Inputs

| Input | Unit | Valid Range | Description |
|---|---:|---:|---|
| Target altitude | ft | 0 to 40,000 | Commanded altitude |
| Current altitude | ft | 0 to 40,000 | Measured aircraft altitude |
| Vertical speed | ft/min | -6,000 to +6,000 | Rate of climb or descent |
| Airspeed | knots | 0 to 500 | Current aircraft speed |
| Altitude sensor valid | Boolean | True / False | Validity of altitude sensor |
| Airspeed sensor valid | Boolean | True / False | Validity of airspeed sensor |

## 8. Outputs

| Output | Unit | Valid Range | Description |
|---|---:|---:|---|
| Pitch command | degrees | -15 to +15 | Nose-down or nose-up command |
| Thrust command | % | 0 to 100 | Engine thrust command |
| System mode | N/A | Normal / Degraded / Fail-safe | Current system operating mode |
| Warning flag | Boolean | True / False | Indicates invalid input or unsafe condition |

## 9. Assumptions
-Aircraft behaviour is simplified and linear.
-Environmental effects such as wind and turbulence are ignored.
-The system is not intended to represent the real Airbus A320 flight control system.
-Values are representative for a commercial aircraft-style scenario.
-The goal is to demonstrate V&V process, not aerodynamic accuracy.
## 10. High-Level Behaviour
If the current altitude is below the target altitude, the system should command positive pitch and increased thrust.
If the current altitude is above the target altitude, the system should command a negative pitch and reduced thrust.
If input data is invalid, the system should enter Degraded or Fail-safe mode depending on the severity of the fault.
## 11. Next Steps
The next project artefact will be:
1. System Requirements Specification
2. Interface Control Document
3. Verification Plan
4. Test Cases
5. Requirements Traceability Matrix
6. Test Report
