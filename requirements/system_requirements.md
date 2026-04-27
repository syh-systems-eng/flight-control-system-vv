# System Requirements Specification (Initial Draft)

## FCS-REQ-001
The system shall accept a target altitude input within the range of 0 to 40,000 ft.

## FCS-REQ-002
The system shall validate that the current altitude input is within the range of 0 to 40,000 ft before processing.

## FCS-REQ-003
The system shall calcuate the altitude error as the difference between target altitude and current altitude.

## FCS-REQ-004
The system shall generate a positive command when the current altitude is below the target altitude, and a negative pitch command when the current altitude is above the target altitude.

## FCS-REQ-005
The system shall limit the pitch command output to a range of -15 degrees to +15 degrees.

## Fault Handling and System Modes
## FCS-REQ-006
The system shall defect when the current altitude input is invalid.

## FCS-REQ-007
The system shall set a warnign flag when any required input data is invalid.

## FCS-REQ-009
The system shall enter Fail-safe mode when critical input data required for control calculation is unavailable.

## FCS-REQ-010
The system shall command a neutral pitch output (0 degress) when operating in Fail-safe mode.

## FCS-REQ-011
The system shall maintain stable pitch control under moderate fluctuations in valid altitude input.

## FCS-REQ-012  
The system shall detect inconsistent or unstable altitude input data.
