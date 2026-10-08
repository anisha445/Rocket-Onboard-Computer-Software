# 🚀 Onboard Flight Computer Software — Verification & Validation

## Overview

The **onboard flight computer is the brain of a launch vehicle**. It runs real-time software responsible for coordinating onboard functions, processing sensor information, monitoring system health, managing interfaces, and supporting reliable flight operations.

Because this software operates in a **real-time and safety-critical environment**, verification requires more than testing individual software functions. The software is progressively verified from the **unit level to integrated hardware and real-time flight-like environments**.

This repository presents a **high-level and generalized view of my work in software verification and reliability of onboard flight computer software**.

---

##  Verification Approach

My verification approach covers multiple levels of testing:

```text
                 Onboard Flight Computer
                          │
                          ▼
                 ┌─────────────────┐
                 │  Unit Testing   │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Integration     │
                 │ Testing         │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Simulated Input │
                 │ Profile Testing │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Hardware-in-    │
                 │ Loop Testing    │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Onboard-in-Loop │
                 │    Testing      │
                 └─────────────────┘
```

### 1. Unit-Level Testing

Verification of individual software functions using:

* Nominal inputs
* Boundary conditions
* Invalid inputs
* Error and failure conditions
* Initialization and reset scenarios
* Expected output verification
* Structural coverage analysis

### 2. Integration-Level Testing

Verification of interactions between software components and onboard interfaces, including:

* Data exchange
* Interface handling
* Sensor data processing
* Health-status handling
* Command and response behavior
* Timing and sequencing
* Error propagation

### 3. Simulated Input Profile Testing

Controlled input profiles are used to reproduce different operating conditions and evaluate software behavior.

Scenarios can include:

* Nominal sensor behavior
* Changing sensor values
* Boundary conditions
* Invalid data
* Communication interruptions
* Sensor failures
* Abnormal operating conditions

### 4. Hardware-in-the-Loop Testing

HIL testing combines **real onboard hardware with real-time simulated systems**.

This allows the flight computer software running on target hardware to be tested against controlled and repeatable system inputs while evaluating:

* Hardware/software interfaces
* Real-time communication
* Sensor data handling
* Timing behavior
* Health monitoring
* Fault responses

### 5. Onboard-in-the-Loop Testing

Onboard-in-the-Loop testing takes the verification closer to actual operational conditions.

The onboard computer and associated interfaces are exercised using controlled or simulated inputs to verify:

* Real-time execution
* Hardware interfaces
* Sensor data processing
* System health monitoring
* Command and response behavior
* Operational and fault scenarios

---

## ⚡ Real-Time Sensor Simulation

Real-time simulation platforms such as **NI CompactRIO (cRIO)** and **Speedgoat** can be used to reproduce sensor and subsystem behavior.

The basic concept is:

```text
        Sensor / System Model
                 │
                 ▼
       ┌────────────────────┐
       │  cRIO / Speedgoat  │
       │   Real-Time Model  │
       └─────────┬──────────┘
                 │
                 │ Real-Time Inputs
                 ▼
       ┌────────────────────┐
       │  Onboard Flight    │
       │      Computer      │
       └─────────┬──────────┘
                 │
                 │ Outputs / Status
                 ▼
          Test & Analysis
```

This provides a controlled and repeatable way to evaluate onboard software against realistic, time-dependent sensor behavior.

---

## 🧪 What I Verify

The verification process focuses on both **nominal and abnormal behavior**.

Examples include:

* Does the software produce the expected output?
* Does it execute within the required timing?
* What happens when sensor data is unavailable?
* How are communication failures detected?
* How is unhealthy subsystem behavior handled?
* Does the software respond correctly to invalid data?
* Are failures reported correctly?
* Does the system transition to the expected state?

The objective is to build confidence that the onboard software behaves **correctly, predictably, and reliably** under expected as well as unexpected conditions.

---

## 🛠️ Technologies & Tools

**Software & Verification**

* C / C++
* Real-Time Operating Systems
* Unit Testing
* Integration Testing
* Structural Coverage
* MC/DC
* Requirements & Design Verification

**Real-Time / Hardware Testing**

* NI CompactRIO (cRIO)
* Speedgoat
* Target Hardware
* Sensor & Interface Simulation
* Hardware-in-the-Loop (HIL)
* Onboard-in-the-Loop Testing

**Analysis & Automation**

* Python
* MATLAB
* Test Data Analysis
* Automated Test Reporting

---

## 👩‍💻 My Role

My work focuses on **software verification, quality, and reliability of real-time onboard flight computer software**.

Key activities include:

* Requirement and design review
* Software verification planning
* Unit-level testing
* Integration testing
* Structural coverage analysis
* Simulated input testing
* HIL and onboard-in-loop testing
* Real-time sensor simulation
* Interface and communication verification
* Health monitoring verification
* Failure and recovery testing
* Test-result analysis
* Verification documentation

---

## Verification Philosophy

> **Test the function. Verify the interface. Challenge the failure path. Validate the real-time behavior.**

The overall objective is to progressively increase confidence in the software as testing moves from **individual functions → integrated software → target hardware → real-time simulated environments → flight-like operation**.

---

## Confidentiality

This repository contains only **generalized technical concepts and methodologies** for professional portfolio and educational purposes.

No proprietary source code, confidential mission data, restricted interfaces, internal documents, or company-sensitive information is included.


     






