# SOC & Incident Response Lab

## Project status
**In progress — Ubuntu server installed and SSH access configured.**

The virtual machine is running in VMware Workstation. Wazuh has
not been installed yet. The next step is to verify available
resources and time synchronization before installing Wazuh.

## Overview
This project documents my progress building a security operations
lab to collect security logs, investigate suspicious activity,
and practice incident response.

The planned monitoring platform is Wazuh. Investigation scenarios
will include failed logins and changes to monitored files.

## Learning goals
- Understand how security logs are collected and analyzed.
- Set up Wazuh and connect a monitored endpoint.
- Generate controlled test events inside my own lab.
- Investigate alerts and distinguish test activity from normal behavior.
- Use Nmap to identify exposed services in the lab.
- Document evidence, findings, and response recommendations.

## Lab environment
| Component | Configuration |
| --- | --- |
| Host operating system | Windows 11 |
| Virtualization platform | VMware Workstation 17 Pro |
| Server operating system | Ubuntu Server 24.04.5 LTS |
| Virtual machine | SOC-Wazuh-Server |
| Allocated resources | 4 vCPUs, 8 GB RAM, 50 GB virtual disk |
| Network mode | NAT |
| Remote administration | SSH from Windows Terminal |

Available storage and memory will be checked before installing
the monitoring platform.

## Tools and their purpose
| Tool | Purpose | Status |
| --- | --- | --- |
| VMware Workstation | Run the lab virtual machine | Configured |
| Ubuntu Server | Host the planned Wazuh installation | Installed |
| OpenSSH | Administer Ubuntu from Windows Terminal | Connection verified |
| Wazuh | Collect logs and investigate security alerts | Planned |
| Monitored endpoint | Generate activity for investigation | Pending selection |
| Nmap | Discover ports and services within the lab | Planned |
| GitHub | Maintain documentation and version history | In use |

## Work completed
- Created the project repository and initial documentation.
- Created an Ubuntu Server virtual machine in VMware.
- Installed Ubuntu and configured a user account.
- Enabled SSH access.
- Compared the server's SSH host fingerprint before accepting
  the first connection.
- Successfully connected from Windows Terminal.
- Ran Ubuntu package update and upgrade checks. At that time,
  nine package upgrades were deferred due to Ubuntu's phased rollout.

## Planned investigation scenarios
These scenarios have not been performed yet.

- **Failed logins:** Generate controlled authentication failures
  and investigate the resulting logs and alerts.
- **File changes:** Modify a designated test file and examine
  file integrity monitoring events.
- **Service discovery:** Scan a designated lab system with Nmap
  and document the exposed services.

Each investigation will document the objective, procedure,
observed evidence, analysis, limitations, and response recommendations.

## Lab boundaries
Testing is limited to systems I own and designate for this lab.

Published documentation will exclude passwords, access tokens,
private keys, and sensitive personal information. Screenshots
and logs will be reviewed before publication.

## Progress
- [x] Create the GitHub repository.
- [x] Write the initial project overview.
- [x] Create the VMware virtual machine.
- [x] Install Ubuntu Server.
- [x] Verify SSH access from Windows.
- [x] Check Ubuntu package updates.
- [ ] Verify resources, available storage, and time synchronization.
- [ ] Document the server setup with reviewed screenshots.
- [ ] Install and configure Wazuh.
- [ ] Connect an endpoint and verify log collection.
- [ ] Run and investigate test scenarios.
- [ ] Write incident reports.
- [ ] Review and finalize the project documentation.

## Lessons learned
- A virtual machine provides a separate operating system for the lab.
- SSH allows remote administration through an encrypted connection.
- Checking the SSH host fingerprint helps verify the server's identity.
- `apt update` refreshes package information; `apt upgrade`
  installs eligible package updates.
- Ubuntu may temporarily defer some updates through phased rollouts.
## Findings and lessons learned
To be added as the lab is built and tested.
