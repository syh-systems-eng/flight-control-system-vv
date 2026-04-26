# System Requirements Specification (Initial Draft)

## FCS-REQ-001
The system shall accept a target altitude input within the range of 0 to 40,000 ft.
</> Markdown

## FCS-REQ-002
The system shall validate that the current altitude input is within the range of 0 to 40,000 ft before processing.
</> Markdown

## FCS-REQ-003
The system shall calcuate the altitude error as the difference between target altitude and current altitude.
</> Markdown

## FCS-REQ-004
The system shall generate a positive command when the current altitude is below the target altitude, and a negative pitch command when the current altitude is above the target altitude.
</> Markdown

## FCS-REQ-005
The system shall limit the pitch command output to a range of -15 degrees to +15 degrees.
