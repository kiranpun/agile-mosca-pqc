# Agile Mosca: Post-Quantum "Security Sidecar" 

**Winner: 1st Place - UoSurrey Hackathon 2026** *Targeting the "Harvest Now, Decrypt Later" (HNDL) Crisis.*

---

##  Project Overview
Agile Mosca is a software-defined security layer designed to protect legacy systems from future quantum threats. By utilising a **Sidecar Proxy** model, we wrap standard TCP/IoT traffic in a **NIST-standard ML-KEM (Lattice-based)** encryption layer.

This allows organisations to meet the **UK NCSC 2035 Deadline** without expensive hardware refreshes or complex code rewrites.

## The Problem
* **HNDL Attacks:** Adversaries are currently "harvesting" encrypted data to decrypt it once Cryptographically Relevant Quantum Computers (CRQCs) are available.
* **Migration Paralysis:** SMEs and local government bodies lack the resources for a "Total Migration" to Post-Quantum Cryptography (PQC).

## Key Features (In Development)
* **Risk-Based Triage:** Automatically identifies "Eternal Data" that requires a PQC shield based on its shelf-life.
* **Hybrid-Encapsulation:** Combines classical RSA/AES with Lattice-based (Kyber) math for dual-layer security.
* **Zero-Code Integration:** Deployable as a Docker sidecar alongside existing legacy applications.

## Tech Stack (2026 Standards)
* **Core:** Python 3.11+ (planned for now) 
* **PQC Library:** `liboqs-python` (Open Quantum Safe) (planned for now) 
* **Infrastructure:** Docker / NGINX (planned for now) 
* **Compliance:** NCSC 2035 Roadmap & FIPS 203 (ML-KEM)

---
*Developed by Team UoSurrey. Built to secure the future of Surrey’s innovation ecosystem.*
