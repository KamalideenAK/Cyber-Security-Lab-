Secure Defender's Sandbox: Pre-configured Windows Domain for Security Analysis

This lab environment provides defenders with a pre-built Windows domain, readily deployable for security training and testing purposes. The domain comes pre-loaded with essential security tools and preconfigured system logging practices, allowing defenders to quickly gain visibility and investigate potential threats.

Important Note: This lab is designed for educational purposes and is deliberately configured to be insecure. Use caution and avoid connecting it to any sensitive networks. Default Vagrant credentials are used for access.

Key Benefits:

- Rapid Deployment: Quickly set up a fully functional Windows domain complete with security tools.
- Enhanced Security Analysis: Pre-configured logging captures detailed user activity and system events for comprehensive analysis.
- Customizable: Easily adapt the environment to your specific training or testing needs.
- Scalable: Expand the domain by adding additional hosts as required.
- Pre-configured Security Tools:

* Microsoft Advanced Threat Analytics (ATA): Installed on the Windows Event Forwarder (WEF) machine for endpoint detection and response (EDR) capabilities. https://www.microsoft.com/en-us/cloud-platform/advanced-threat-analytics
* Splunk Forwarder: Pre-installed on all systems to collect and forward logs for centralized analysis.
* Custom Group Policy Object (GPO): Enforces a comprehensive Windows auditing configuration to capture command line processes, system events, and more.
* Palantir Integration: Windows Event Forwarding subscriptions and custom channels streamline log collection for Palantir analysis. http://github.com/palantir/windows-event-forwarding
* Powershell Script Logging: Tracks script execution and saves logs for review. \\wef\pslogs
* osquery: Pre-configured on all hosts for detailed system information gathering with secure TLS communication to a central Fleet server. https://fleetdm.com/ https://github.com/palantir/osquery-configuration 
* Sysmon: Installed with a robust configuration for enhanced system monitoring and threat detection. https://github.com/olafhartong/sysmon-modular
* AutorunsToWinEventLog: Automatically logs all autostart entries for analysis of potential startup threats.
* Network Security Tools: Zeek and Suricata provide comprehensive network traffic monitoring and alerting.
* Apache Guacamole: Enables convenient remote access to all hosts within the domain directly from your web browser.
This pre-configured environment empowers defenders to streamline security analysis, gain deep insight into system activity, and effectively detect and respond to potential security threats. https://github.com/palantir/windows-event-forwarding/tree/master/AutorunsToWinEventLog

********************************************************************************************************************************************************************************************************************************************************************************
********************************************************************************************************************************************************************************************************************************************************************************
Building the Lab 

When preparing to build DetectionLab locally, be sure to use the prepare.[sh|ps1] scripts inside of the Vagrant folder to ensure your system passes the prerequisite checks for building lab.

- Prerequisites https://www.detectionlab.network/introduction/prerequisites/
* MacOS - Virtualbox or VMware Fusion https://www.detectionlab.network/deployment/macosvm/ 
Windows - Virtualbox or VMware Workstation https://www.detectionlab.network/deployment/windowsvm/
Linux - Virtualbox or VMware Workstation  https://www.detectionlab.network/deployment/linuxvm/
AWS via Terraform 
Azure via Terraform & Ansible
ESXi via Terraform & Ansible
HyperV
LibVirt
Proxmox

