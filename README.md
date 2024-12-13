# Unified Repository for MFA Phishing Research

This repository contains all the components used in our research and demonstrations on the vulnerabilities of FIDO2 multi-factor authentication (MFA) systems under phishing and adversary-in-the-middle (AITM) attacks. The included sub-repositories focus on different aspects of the study, from environment setup to proof-of-concept attacks and data collection.

## Table of Contents
1. [Overview of Included Repositories](#overview-of-included-repositories)
2. [Purpose](#purpose)
3. [Repository Descriptions](#repository-descriptions)
4. [Getting Started](#getting-started)

<br>

## Overview of Included Repositories
This unified repository consolidates the following sub-repositories:
- [Guac-Setup](#guac-setup)
- [Hardware-FIDO2-Implementation-Demo](#hardware-fido2-implementation-demo)
- [RCA-Attack-Demo](#rca-attack-demo)
- [RCA-PoC](#rca-poc)
- [RWAP-VM](#rwap-vm)
- [Timmer](#timmer)

<br>

## Purpose
The goal of this repository is to provide:
- A comprehensive setup for simulating and analyzing vulnerabilities in FIDO2 MFA systems.
- Tools for demonstrating the potential exploitation of secure environments.
- Data collection utilities for performance analysis.

<br>

<br>

## Repository Descriptions

### Guac-Setup
This repository contains setup scripts and instructions for deploying Guacamole, a remote desktop gateway. It is used to create a virtual environment where phishing attacks can be demonstrated through rogue Wi-Fi access points and adversary-controlled virtual machines. 

**Why it's included**: Guac-Setup facilitates the environment for conducting phishing and AITM attacks in a controlled setup.

---

<br>

### Hardware-FIDO2-Implementation-Demo
This demo simulates the authentication flow of FIDO2 using a YubiKey-like device. It highlights the cryptographic challenge-response mechanisms and demonstrates the phishing-resistant nature of hardware-backed MFA systems.

**Why it's included**: This repository showcases the expected secure behavior of FIDO2 MFA systems and serves as a baseline for evaluating attack scenarios.

---

<br>

### RCA-Attack-Demo
This repository demonstrates a proof-of-concept attack where a rogue access point is used to intercept and manipulate HTTPS traffic. It highlights vulnerabilities in MFA systems when combined with malicious certificate authorities and DNS spoofing.

**Why it's included**: RCA-Attack-Demo illustrates real-world attack scenarios where FIDO2 MFA protections can be bypassed.

---

<br>

### RCA-PoC
The RCA-PoC repository simulates the network interactions between a victim device, rogue access point, DNS server, and a malicious server. It validates the feasibility of phishing and AITM attacks through an end-to-end proof of concept.

**Why it's included**: This repository provides the technical foundation and validation for the attack scenarios discussed in the research.

---

<br>

### RWAP-VM
This repository contains configuration files and scripts for setting up a Rogue Wi-Fi Access Point (RWAP) using tools like `mitmproxy` and `hostapd`. It supports the execution of attacks by enabling DNS manipulation and HTTPS interception.

**Why it's included**: RWAP-VM is essential for configuring the attack infrastructure and ensuring the attack scenarios can be reproduced.

---

<br>

### Timmer
This repository contains scripts to measure and compare load times for direct and proxied (via MITM) network configurations. It uses Selenium with ChromeDriver to collect performance metrics.

**Why it's included**: Timmer provides data to analyze the performance impact of the attack infrastructure, adding quantitative insights to the research.

---

<br>

## Getting Started
Each sub-repository contains its own `README.md` with detailed setup instructions. Clone this repository and refer to the individual README files to set up and run each component:

```bash
# Clone the unified repository
git clone https://github.com/Unified-MFA-Research/Unified-Repo.git

# Navigate to a specific repository
cd Unified-Repo/Guac-Setup
```

Ensure that all dependencies are installed as per the instructions in each sub-repository. The repositories are designed to work together, with each serving a distinct role in the overall research and demonstration framework.
