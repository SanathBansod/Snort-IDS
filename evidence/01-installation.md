# Evidence 01 — Snort Installation

## Objective

The objective of this step was to install Snort on the authorized Kali Linux laboratory machine and verify that the installation was successful.

## Environment

| Parameter | Details |
|---|---|
| Operating System | Kali Linux |
| Tool | Snort |
| Assessment Type | Authorized Security Laboratory |

## Installation

The system package repository was updated before installing Snort.

### Update Package Repository

    sudo apt update

The package repository information was refreshed to ensure that the available package information was current.

### Install Snort

    sudo apt install snort -y

The Snort package and its required dependencies were installed on the Kali Linux laboratory machine.

## Installation Verification

After installation, the Snort version was checked.

### Command

    snort -V

The command displays the installed Snort version and confirms that the Snort executable is available.

## Result

The Snort installation completed successfully.

The `snort -V` command returned the installed Snort version, confirming that Snort was available and ready for the configuration phase.

## Security Relevance

Installing Snort is the first step in establishing a network-based Intrusion Detection System.

Once installed and configured, Snort can inspect network traffic and compare observed packets against detection rules.

## Evidence Screenshot

The following screenshot provides evidence of the Snort installation and version verification.

![Snort Installation](../screenshots/01-installation.png)

## Conclusion

Snort was successfully installed on the authorized Kali Linux laboratory machine and the installation was verified using the Snort version command.

The system is ready for the configuration and rule-development phases of the IDS practical.

## Authorization

This activity was performed exclusively within an authorized cybersecurity laboratory environment for educational and security-training purposes.

No unauthorized systems were targeted.
