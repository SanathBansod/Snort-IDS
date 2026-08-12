# Snort IDS — Intrusion Detection System

> Hands-on Snort IDS laboratory covering installation, configuration, custom detection rules, ICMP detection, port-scan detection, SSH brute-force detection, and alert analysis.

---

## 📌 Project Overview

This project documents a practical Intrusion Detection System (IDS) laboratory using **Snort**.

The objective is to understand how Snort can monitor network traffic, apply custom detection rules, and generate alerts when suspicious or unauthorized activity is observed in an authorized laboratory environment.

The practical covers:

- Snort installation
- Snort configuration
- Custom Snort rules
- ICMP traffic detection
- Port-scan detection
- SSH brute-force detection
- Alert generation and analysis

---

## 🧪 Lab Environment

| Component | Details |
|---|---|
| IDS | Snort |
| Operating System | Kali Linux |
| Network Environment | Authorized Virtual Lab |
| Detection Type | Network-based IDS |
| Assessment Type | Authorized Security Laboratory |

---

## 🔐 Authorization

All activities documented in this repository are performed only within an authorized and controlled cybersecurity laboratory environment.

The detection tests are intended for educational and defensive security training purposes.

No unauthorized systems are targeted.

---

# 🔎 Practical Methodology

The Snort IDS practical follows this workflow:

    Installation
         ↓
    Configuration
         ↓
    Custom Rules
         ↓
    ICMP Detection
         ↓
    Port Scan Detection
         ↓
    SSH Brute Force Detection
         ↓
    Alert Generation
         ↓
    Alert Analysis

---

# 1️⃣ Snort Installation

## Objective

Install Snort on the authorized Kali Linux laboratory machine and verify that the installation is working correctly.

## Installation

The Snort package was installed using the system package manager.

After installation, the Snort version was verified to confirm that the installation was successful.

## Verification

The installation was verified using the Snort version command.

The version information confirms that Snort is available on the system and ready for configuration.

## Evidence

[Evidence 01 — Installation](evidence/01-installation.md)

---

# 2️⃣ Snort Configuration

## Objective

Configure Snort to monitor the appropriate network interface and load the custom detection rules used during the laboratory exercise.

The configuration process includes:

- Identifying the monitoring interface
- Configuring the protected network
- Reviewing the Snort configuration
- Loading the custom rules
- Testing the configuration before starting detection

## Network Monitoring

Snort monitors network traffic passing through the selected interface.

The monitoring interface must be correctly identified before starting the IDS.

## Configuration Verification

The Snort configuration is tested before running the detection engine to identify configuration or rule errors.

## Evidence

[Evidence 02 — Configuration](evidence/02-configuration.md)

---

# 3️⃣ Custom Snort Rules

## Objective

Create custom Snort rules to detect specific network activities in the authorized laboratory environment.

The custom rules cover:

- ICMP traffic
- Port scanning
- SSH brute-force activity

Custom rules allow Snort to identify traffic patterns that are relevant to a particular security-monitoring requirement.

## Rule Structure

A Snort rule generally contains:

    Action
    Protocol
    Source IP
    Source Port
    Direction
    Destination IP
    Destination Port
    Rule Options

Example structure:

    alert icmp any any -> any any (msg:"ICMP Traffic Detected"; sid:1000001; rev:1;)

The exact rules used in the laboratory are documented in the custom-rules evidence.

## Evidence

[Evidence 03 — Custom Rules](evidence/03-custom-rules.md)

---

# 4️⃣ ICMP Detection

## Objective

Detect ICMP traffic using a custom Snort rule.

ICMP traffic is commonly associated with network diagnostic operations such as `ping`, but unexpected ICMP activity can also provide useful information during security monitoring.

## Detection Workflow

    ICMP Traffic
         ↓
    Snort Rule
         ↓
    Rule Match
         ↓
    Alert Generated
         ↓
    Alert Analysis

## Test

An authorized ICMP test was performed against the laboratory environment.

The custom Snort rule was configured to generate an alert when matching ICMP traffic was observed.

## Expected Result

Snort should generate an alert indicating that the configured ICMP traffic pattern was detected.

## Evidence

[Evidence 04 — ICMP Detection](evidence/04-icmp-detection.md)

---

# 5️⃣ Port Scan Detection

## Objective

Detect port-scanning activity using Snort in the authorized laboratory environment.

Port scanning is a common reconnaissance technique used to identify open ports and services on a network host.

## Detection Workflow

    Port Scan
         ↓
    Network Packets
         ↓
    Snort Detection Rule
         ↓
    Rule Match
         ↓
    Alert Generated

## Test

An authorized port-scan test was performed against the laboratory target.

Snort monitored the resulting traffic and evaluated it against the configured detection rule.

## Expected Result

Snort should generate an alert when the traffic matches the configured port-scan detection condition.

## Evidence

[Evidence 05 — Port Scan Detection](evidence/05-port-scan-detection.md)

---

# 6️⃣ SSH Brute-Force Detection

## Objective

Detect repeated SSH authentication attempts using a custom Snort rule in the authorized laboratory environment.

Repeated authentication attempts can indicate password-guessing or brute-force activity.

## Detection Concept

    Repeated SSH Attempts
             ↓
       Network Traffic
             ↓
       Snort Rule
             ↓
        Threshold
             ↓
       Alert Generated

## Test

An authorized SSH authentication-testing activity was performed against the laboratory target.

Snort monitored the traffic and evaluated it against the configured detection rule.

## Expected Result

When the configured threshold or traffic pattern is reached, Snort should generate an alert indicating suspected SSH brute-force activity.

## Evidence

[Evidence 06 — SSH Brute Force Detection](evidence/06-ssh-brute-force-detection.md)

---

# 7️⃣ Alerts

## Objective

Review and analyze alerts generated by Snort during the laboratory tests.

The alerts provide evidence that Snort successfully detected traffic matching the configured custom rules.

## Alert Categories

The laboratory generated alerts for:

- ICMP activity
- Port-scan activity
- SSH brute-force activity

## Alert Information

A Snort alert can provide information such as:

- Timestamp
- Alert message
- Protocol
- Source address
- Source port
- Destination address
- Destination port
- Rule identifier

## Alert Analysis

Each generated alert was reviewed to determine:

1. Which rule triggered.
2. What traffic caused the rule match.
3. Source and destination information.
4. Whether the observed activity matched the expected laboratory test.

## Evidence

[Evidence 07 — Alerts](evidence/07-alerts.md)

---

# 📊 Detection Summary

| Activity | Detection Method | Expected Result |
|---|---|---|
| ICMP | Custom Snort Rule | ICMP Alert |
| Port Scan | Custom Snort Rule | Port-Scan Alert |
| SSH Brute Force | Custom Snort Rule | SSH Brute-Force Alert |

---

# 🧠 Key Learning Outcomes

This practical demonstrates how a network-based IDS can be configured to identify specific traffic patterns.

The major concepts covered are:

- IDS installation
- Snort configuration
- Network monitoring
- Custom detection rules
- Rule matching
- ICMP detection
- Reconnaissance detection
- SSH attack detection
- Alert generation
- Alert analysis

The practical workflow is:

    Network Traffic
          ↓
    Snort Monitoring
          ↓
    Rule Evaluation
          ↓
    Rule Match
          ↓
    Alert
          ↓
    Security Analysis

---

# 🎯 Skills Demonstrated

- Snort IDS
- Network traffic monitoring
- IDS configuration
- Custom Snort rules
- ICMP detection
- Port-scan detection
- SSH brute-force detection
- Alert analysis
- Network security monitoring
- Security event investigation
- Linux security tooling

---

# 📂 Repository Structure

    Snort-IDS/
    │
    ├── README.md
    │
    ├── evidence/
    │   ├── 01-installation.md
    │   ├── 02-configuration.md
    │   ├── 03-custom-rules.md
    │   ├── 04-icmp-detection.md
    │   ├── 05-port-scan-detection.md
    │   ├── 06-ssh-brute-force-detection.md
    │   └── 07-alerts.md
    │
    └── screenshots/
        ├── 01-installation.png
        ├── 02-configuration.png
        ├── 03-custom-rules.png
        ├── 04-icmp-alert.png
        ├── 05-port-scan-alert.png
        ├── 06-ssh-brute-force-alert.png
        └── 07-alerts.png

---

# 📸 Evidence

All practical evidence and screenshots are maintained under the `evidence/` and `screenshots/` directories.

Each evidence document describes:

- Objective
- Methodology
- Commands
- Configuration
- Detection result
- Security relevance
- Screenshot evidence
- Conclusion

---

# ⚠️ Disclaimer

This project is intended strictly for authorized cybersecurity education, defensive security training, and laboratory testing.

The detection tests and security-monitoring activities documented in this repository must only be performed against systems and networks for which explicit authorization has been obtained.

No unauthorized systems are targeted.
