# Evidence 01 — Snort Installation

## Objective

The objective of this step was to install and verify Snort 3 on the Kali Linux machine for use as a network-based Intrusion Detection System (IDS) in an authorized cybersecurity laboratory environment.

## Environment

| Parameter | Details |
|---|---|
| Operating System | Kali Linux |
| Security Tool | Snort 3 |
| Tool Type | Network IDS/IPS |
| Assessment Type | Authorized Security Laboratory |

## Package Repository Update

The system package repository information was updated before installing Snort.

### Command

    sudo apt update

This ensured that the local package information was refreshed before installation.

## Snort Installation

Snort was installed using the Kali Linux package manager.

### Command

    sudo apt install snort -y

The command installs Snort and its required package dependencies.

## Installation Verification

After installation, the installed Snort version was verified.

### Command

    snort -V

The command displayed the installed Snort version and confirmed that the Snort executable was available from the command line.

## Verification Result

The installed Snort version was:

    Snort++ 3.12.2.0

The version check confirmed that Snort 3 was successfully installed and available for subsequent configuration and detection testing.

## Security Relevance

Snort is a network intrusion detection and prevention system capable of inspecting network traffic and applying detection rules.

Successful installation is the first step before configuring the IDS, creating custom detection rules, monitoring traffic, and generating security alerts.

## Evidence Screenshot

![Snort Installation](../screenshots/01-installation.png)

The screenshot shows the installed Snort version obtained using the `snort -V` command.

## Result

Snort 3 was successfully installed and verified on the Kali Linux laboratory machine.

The installation is ready for the configuration phase.

## Conclusion

The Snort IDS installation was successfully completed and verified.

The next phase will configure Snort 3 for network traffic monitoring and custom rule processing.

## Authorization

This activity was performed exclusively within an authorized cybersecurity laboratory environment for educational and security-training purposes.

No unauthorized systems were targeted.
