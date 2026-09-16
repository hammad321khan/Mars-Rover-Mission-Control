# Non-Functional Requirements

## Mars Rover Mission Control

Non-functional requirements describe how well the system should operate.

| ID | Non-Functional Requirement |
|---|---|
| NFR-01 | Command processing should normally complete within 5 seconds after a command is received by the rover. |
| NFR-02 | Only authenticated Mission Control operators shall be permitted to issue rover commands. |
| NFR-03 | The system shall handle communication delays without repeatedly sending unconfirmed commands. |
| NFR-04 | The system shall support communication with multiple rovers simultaneously. |

## Requirement Details

### NFR-01 — Performance

Command processing should normally complete within 5 seconds after a command is received by the rover.

### NFR-02 — Security

Only authenticated Mission Control operators shall be permitted to issue rover commands.

### NFR-03 — Communication Reliability

The system shall handle several-minute communication delays without repeatedly sending unconfirmed commands.

### NFR-04 — Scalability

The system shall support communication with multiple rovers simultaneously.
