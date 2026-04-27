# System Block Diagram

This diagram shows the high-level system boundary for the Simplified Flight Control System — Altitude Hold Function.

```mermaid
flowchart LR

    A[Target Altitude Command] --> SUT
    B[Current Altitude] --> SUT
    C[Vertical Speed] --> SUT
    D[Airspeed] --> SUT
    E[Sensor Validity Flags] --> SUT

    subgraph SUT[Altitude Hold Control Function]
        F[Input Validation]
        G[Altitude Error Calculation]
        H[Control Logic]
        I[Mode Management]
        J[Safety Limiting]
    end

    SUT --> K[Pitch Command]
    SUT --> L[Thrust Command]
    SUT --> M[System Mode]
    SUT --> N[Warning Flag]
```
## System Boundary

The Altitude Hold Control Function is treated as the System Under Test.

Inputs such as aircraft state data and sensor validity flags are received from external systems. The function validates these inputs, calculates altitude error, applies control logic, manages system mode, and outputs pitch/thrust commands with warning status.

## Notes

This diagram is intentionally simplified. It does not represent a real aircraft architecture or Airbus A320 flight control implementation.
