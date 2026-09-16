# Mars-Rover-Mission-Control
# 🚀 Mars Rover Mission Control

## Software Requirements Engineering Task

A Software Requirements Engineering task based on the analysis and management of requirements for a **Mars Rover Mission Control System**.

Mars Rover Mission Control is a software system designed to remotely control and monitor exploration rovers on Mars.

The rover communicates with Mission Control through a communication link that has:

* Limited communication bandwidth
* Several minutes of communication delay
* Possible temporary communication interruptions

Because of these limitations, commands cannot simply be sent repeatedly without confirmation.

The system must provide reliable command execution, rover monitoring, security, safety, fault handling, and event logging.

---

## 🎯 System Objectives

The system is designed to:

* Send movement commands to rovers
* Receive rover location and health information
* Detect communication failures
* Prevent unauthorized commands
* Automatically place the rover into Safe Mode during critical faults
* Receive command execution status
* Store mission events for later investigation
* Support communication with multiple rovers simultaneously
* Continue operating during temporary communication interruptions

---

# 📋 Mission 1 — Analyze the Engineering Note

## Functional Requirements

Functional Requirements describe **what the system shall do**.

| ID        | Functional Requirement                                                                             |
| --------- | -------------------------------------------------------------------------------------------------- |
| **FR-01** | The rover shall receive commands from Mission Control and execute valid commands.                  |
| **FR-02** | The rover shall report its current position, battery level, temperature, and communication status. |
| **FR-03** | Only authenticated Mission Control operators shall be allowed to issue commands.                   |
| **FR-04** | The system shall reject invalid or unauthorized commands.                                          |
| **FR-05** | If the rover detects a critical battery or thermal condition, it shall enter Safe Mode.            |
| **FR-06** | Mission Control shall receive command execution status.                                            |
| **FR-07** | All commands and critical rover events shall be recorded with timestamp and operator ID.           |
| **FR-08** | The system shall continue operating despite temporary communication interruptions.                 |

---

## ⚙️ Non-Functional Requirements

Non-Functional Requirements describe **how the system should perform**.

| ID         | Non-Functional Requirement                                                                             |
| ---------- | ------------------------------------------------------------------------------------------------------ |
| **NFR-01** | Command processing should normally complete within 5 seconds after a command is received by the rover. |
| **NFR-02** | Only authenticated Mission Control operators shall be permitted to issue rover commands.               |
| **NFR-03** | The system shall handle communication delays without repeatedly sending unconfirmed commands.          |
| **NFR-04** | The system shall support communication with multiple rovers simultaneously.                            |

---

# 🔄 Mission 2 — Change Requests

Mission Control introduced three changes to the original requirements.

---

## 🆘 CR-01 — Emergency Safety

### Original Requirement

**FR-04**

> The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

### Updated Requirement

**FR-04**

> The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

### Change

The requirement now includes:

* A specific emergency condition
* Battery temperature threshold
* Battery capacity threshold
* A maximum response time of **3 seconds**

### Result

The requirement is now:

* Specific
* Measurable
* Testable
* Safety-focused

---

# 🛰️ CR-02 — Mission Expansion

### Original Requirement

**NFR-04**

> The system shall support communication with multiple rovers simultaneously.

### Updated Requirement

**NFR-04**

> The system shall support at least 20 simultaneously connected rovers.

### Change

The vague word **"multiple"** has been replaced with the measurable value **20**.

### Result

The requirement is now:

* Specific
* Measurable
* Testable
* Scalable

---

# 🔐 CR-03 — Security Upgrade

### Original Requirement

**NFR-02**

> Only authenticated Mission Control operators shall be permitted to issue rover commands.

### Updated Requirement

**NFR-02**

> The system shall require authenticated and role-authorized operators before accepting rover commands.

### Change

The security requirement now includes:

1. Authentication
2. Role-based authorization

### Result

The system provides stronger access control for rover commands.

---

# 📊 Change Request Summary

| Change Request | Requirement | Original                                            | Updated                                                 |
| -------------- | ----------- | --------------------------------------------------- | ------------------------------------------------------- |
| **CR-01**      | FR-04       | Safe Mode during critical battery/thermal condition | Safe Mode within **3 seconds**                          |
| **CR-02**      | NFR-04      | Support multiple rovers                             | Support **at least 20** simultaneously connected rovers |
| **CR-03**      | NFR-02      | Authenticated operators                             | Authenticated **and role-authorized** operators         |

---

# 🧪 Verification & Testing

The updated requirements can be verified using test cases.

## Test Case 1 — Emergency Safe Mode

**Requirement:** FR-04

**Action:**
Trigger a critical battery or thermal condition.

**Expected Result:**
The rover enters Safe Mode within **3 seconds**.

---

## Test Case 2 — Multiple Rover Support

**Requirement:** NFR-04

**Action:**
Connect 20 rovers simultaneously.

**Expected Result:**
The system successfully supports communication with all 20 connected rovers.

---

## Test Case 3 — Role-Based Authorization

**Requirement:** NFR-02

**Action:**
Attempt to issue a rover command using different types of users.

| User Type                                  | Expected Result |
| ------------------------------------------ | --------------- |
| Unauthenticated user                       | ❌ Rejected      |
| Authenticated but unauthorized user        | ❌ Rejected      |
| Authenticated and role-authorized operator | ✅ Accepted      |

---

# 🔍 Requirements Quality Analysis

The change requests improve the quality of the original requirements.

| Requirement | Original Issue             | Improvement                      |
| ----------- | -------------------------- | -------------------------------- |
| **FR-04**   | No response time specified | Adds **3-second** response limit |
| **NFR-04**  | "Multiple" is vague        | Specifies **20 rovers**          |
| **NFR-02**  | Authentication only        | Adds **role authorization**      |

The updated requirements are more:

* Specific
* Measurable
* Testable
* Unambiguous

---

# 🧩 Requirement Classification

| Requirement                  | Category    |
| ---------------------------- | ----------- |
| Rover command execution      | Functional  |
| Rover health reporting       | Functional  |
| Command authentication       | Security    |
| Command validation           | Functional  |
| Safe Mode                    | Safety      |
| Command execution status     | Functional  |
| Event logging                | Functional  |
| Communication recovery       | Reliability |
| 5-second processing          | Performance |
| Role authorization           | Security    |
| Communication delay handling | Reliability |
| 20 simultaneous rovers       | Scalability |

---

# 📁 Repository Structure

```text
mars-rover-mission-control/
│
├── README.md
│
├── functional-requirements.md
│
├── non-functional-requirements.md
│
├── change-requests.md
│
└── requirements-analysis.md
```

---

# 🎓 Learning Outcomes

After completing this task, the student should be able to:

* Identify Functional Requirements
* Identify Non-Functional Requirements
* Classify software requirements
* Analyze requirement changes
* Identify ambiguous requirements
* Convert vague requirements into measurable requirements
* Understand security requirements
* Understand safety requirements
* Create testable requirements
* Perform basic change impact analysis

---

# 👨‍💻 Author

**Hammad Khan**

**Roll No:** 061

**Course:** Software Requirements Engineering

**Task:** Mars Rover Mission Control — Requirements Analysis & Change Management

---

# ✅ Conclusion

The Mars Rover Mission Control system requires reliable communication, secure command handling, fault detection, safety mechanisms, and event logging.

The change requests make the original requirements more precise and measurable:

* Safe Mode must activate within **3 seconds** during defined critical conditions.
* The system must support **at least 20 simultaneously connected rovers**.
* Rover commands require both **authentication and role authorization**.

These changes make the requirements easier to implement, verify, validate, and test.
