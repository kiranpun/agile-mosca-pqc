 # Agile Mosca: Post-Quantum "Security Sidecar" 

*📐 Project Status: Architecture & MVP Design Phase > Originally conceptualised at SheHacksSurrey (2026), organised by the Surrey Cyber Security Cluster. This repository currently serves as the architectural blueprint and upcoming MVP specification for a hybrid Post-Quantum security proxy.*

---

##  Project Overview
Agile Mosca is a proposed software-defined "Security Sidecar" architecture designed to protect legacy, unpatchable systems from quantum threats. By utilising a zero-code proxy model, the goal is to wrap standard TCP/IoT traffic in a NIST-standard ML-KEM (Lattice-based) encryption layer.

Our core engineering objective is to build a practical tool for Cryptographic Agility. Crucially, the Agile Mosca architecture is designed to offload the compliance burden, allowing infrastructure operators to defer their cryptographic testing to the proxy and meet the UK NCSC 2035 migration deadlines without replacing expensive hardware.

## The Engineering & Compliance Challenge
* **HNDL Attacks:** Adversaries are currently "harvesting" encrypted data to decrypt it once Cryptographically Relevant Quantum Computers (CRQCs) are available.
* **Migration Paralysis:** SMEs, satellite operators, and industrial facilities lack the budget and engineering resources for a "Rip and Replace" migration to Post-Quantum Cryptography (PQC).
* **The Audit Nightmare:** Organisations lack the in-house cryptographic expertise to validate and test new mathematical models against NCSC/NIST standards.

## Target Architecture Variants
We recognise that a factory sensor has vastly different compute constraints than a standard workstation. The MVP is being scoped into two target tiers:

* **Agile Mosca Core:** Designed for legacy workstations and standard servers.

* **Agile Mosca Edge:** A lightweight variant optimised for low-bandwidth environments (IoT, satellite telemetry). The design explicitly specifies Elliptic Curve (ECC) primitives in its hybrid handshake to minimise power draw and bandwidth overhead.

  
## Proposed MVP Capabilities
* **NIST-Validated Core:** The logic is being built exclusively around finalised NIST PQC standards, primarily FIPS 203 (ML-KEM).
* **Zero-Code Integration:** Designed to be deployable as a Docker sidecar alongside existing applications, requiring zero code modifications on the host device.
* **Hybrid-Encapsulation:** The target handshake combines classical cryptography (ECC/AES) with Lattice-based math (ML-KEM/Kyber) for dual-layer security.
* **Automated Audit Logging:** The system will generate cryptographic deployment logs for network admins to demonstrate transitional readiness to compliance auditors.

## Project Roadmap
* **Phase 0** - Systems Design (Current): Architectural mapping, algorithm selection, and scoping the logic for risk-based data routing.
* **Phase 1** - Hybrid MVP Build: Developing the Python/liboqs core and deploying the initial ECC + ML-KEM Docker proxy in a local test environment.
* **Phase 2** - Pure PQC Target (2030+): Designing the remote update mechanism to deprecate the classical hybrid layer, transitioning to pure ML-KEM well ahead of the NCSC 2035 mandate.

## Tech Stack (2026 Standards)
* **Core:** Python 3.11+ (planned for now) 
* **PQC Library:** `liboqs-python` (Open Quantum Safe) (planned for now) 
* **Infrastructure:** Docker / NGINX (planned for now) 
* **Compliance:** NCSC 2035 Roadmap & FIPS 203 (ML-KEM)

---
*Built to secure the future.*
