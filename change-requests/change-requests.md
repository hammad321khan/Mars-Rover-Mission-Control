# Change Requests

## Mars Rover Mission Control

Mission Control introduced three changes to the original requirements.

---

## CR-01 — Emergency Safety

### Original Requirement

**FR-04**

The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

### Updated Requirement

**FR-04**

The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

### Impact

The requirement is now:

- Specific
- Measurable
- Testable
- Safety-focused

---

## CR-02 — Mission Expansion

### Original Requirement

**NFR-04**

The system shall support communication with multiple rovers simultaneously.

### Updated Requirement

**NFR-04**

The system shall support at least 20 simultaneously connected rovers.

### Impact

The vague term "multiple" has been replaced with a measurable value of 20 rovers.

The requirement is now:

- Specific
- Measurable
- Testable
- Scalable

---

## CR-03 — Security Upgrade

### Original Requirement

**NFR-02**

Only authenticated Mission Control operators shall be permitted to issue rover commands.

### Updated Requirement

**NFR-02**

The system shall require authenticated and role-authorized operators before accepting rover commands.

### Impact

The security requirement now includes:

1. Authentication
2. Role-based authorization

This provides stronger access control for rover commands.

---

# Change Request Summary

| Change Request | Requirement | Original | Updated |
|---|---|---|---|
| CR-01 | FR-04 | Safe Mode during critical battery/thermal condition | Safe Mode within 3 seconds |
| CR-02 | NFR-04 | Multiple rovers | At least 20 simultaneously connected rovers |
| CR-03 | NFR-02 | Authenticated operators | Authenticated and role-authorized operators |
