# Evidence 02 — Snort Configuration

## Objective

The objective of this step was to verify and configure Snort 3 for network traffic monitoring in the authorized cybersecurity laboratory environment.

## Snort Version

The installed Snort version was identified using:

    snort -V

The laboratory system is running:

    Snort++ 3.12.2.0

## Configuration Model

Snort 3 uses Lua-based configuration files.

The primary configuration file is:

    snort.lua

The configuration controls how Snort processes network traffic, loads rules, and handles detection and logging.

## Configuration Validation

The Snort configuration was validated before beginning the detection tests.

The configuration validation completed successfully with zero warnings.

### Validation Result

    Snort successfully validated the configuration (with 0 warnings).

This confirmed that the active Snort configuration was syntactically valid and could be processed by the Snort engine.

## Network Interface

The network interface used for monitoring was identified on the Kali Linux laboratory machine.

The interface was verified before starting live traffic detection.

### Command

    ip -br addr

The command was used to identify available network interfaces and their assigned addresses.

## Configuration File

The Snort 3 Lua configuration file was located and reviewed before running the IDS.

The configuration was used as the base configuration for the subsequent custom-rule detection exercises.

## Rule Loading

Snort 3 supports loading custom rules from separate `.rules` files.

The custom rules created for this project will be loaded during the detection phase.

The rule categories include:

- ICMP detection
- Port-scan detection
- SSH brute-force detection

## Configuration Test

Before running Snort against live laboratory traffic, the configuration was validated.

The successful validation confirmed:

- The configuration file could be loaded.
- The Snort configuration contained no validation warnings.
- The Snort engine was ready for the next stage.
- Custom detection rules could be tested against the configured environment.

## Security Relevance

Correct configuration is essential for an IDS because the configuration determines how Snort processes network traffic and loads detection rules.

A configuration error can prevent Snort from starting or can result in detection rules not being loaded correctly.

## Evidence Screenshot

The following screenshot provides evidence of the Snort 3 configuration validation.

![Snort Configuration Validation](../screenshots/02-configuration.png)

## Result

Snort 3.12.2.0 successfully validated the active configuration with zero warnings.

The Snort installation is therefore ready for the custom-rule development and detection phases.

## Conclusion

The Snort 3 configuration was successfully validated in the authorized laboratory environment.

The next phase is to create and test custom Snort rules for ICMP traffic, port scanning, and SSH brute-force detection.

## Authorization

This activity was performed exclusively within an authorized cybersecurity laboratory environment for educational and security-training purposes.

No unauthorized systems were targeted.
