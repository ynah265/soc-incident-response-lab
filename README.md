# SOC & Incident Response Lab

## Project status
**In progress — Wazuh installed and dashboard access verified.**

Completed the Ubuntu Server setup and installed the Wazuh server,
indexer, and dashboard. Verified that all three services are active
and successfully accessed the dashboard from Windows.

Next: connect the first monitored endpoint and verify log collection.

## Overview
This project documents my progress building a security operations
lab to collect security logs, investigate suspicious activity,
and practice incident response.

The monitoring platform is Wazuh. Planned investigation scenarios
include failed logins, changes to monitored files, and service discovery.

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

Before installing Wazuh, verified CPU allocation, available memory,
disk space, and clock synchronization. Ubuntu reported approximately
40 GB of available disk space, and Windows reported 64.4 GB free
on C:. These measurements were taken before the Wazuh installation.

The server uses UTC, with network time synchronization active.

## Tools and their purpose
| Tool | Purpose | Status |
| --- | --- | --- |
| VMware Workstation | Run the lab virtual machine | Configured |
| Ubuntu Server | Host Wazuh's central components | Installed |
| OpenSSH | Administer Ubuntu from Windows Terminal | Connection verified |
| Wazuh | Collect and analyze security events | Installed; dashboard access verified |
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
- Checked Ubuntu package updates and applied available upgrades.
- Restarted Ubuntu when a reboot was required.
- Verified resources, available storage, and time synchronization.
- Installed the Wazuh server, indexer, and dashboard using the
  official installation assistant.
- Verified that all three Wazuh services report `active`.
- Successfully logged in to the Wazuh dashboard.
- Disabled the Wazuh package repository to prevent accidental
  upgrades. Ubuntu's update sources remain enabled.

## Setup evidence
Screenshots will be added after reviewing them for sensitive information.

Planned evidence:
- Terminal output showing all three Wazuh services as `active`.
- Initial Wazuh dashboard showing successful access.

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

Generated installation files containing credentials, including
`wazuh-install-files.tar`, will not be uploaded to this repository.

## Progress
- [x] Create the GitHub repository.
- [x] Write the initial project overview.
- [x] Create the VMware virtual machine.
- [x] Install Ubuntu Server.
- [x] Verify SSH access from Windows.
- [x] Check Ubuntu package updates.
- [x] Verify resources, available storage, and time synchronization.
- [x] Install Wazuh server, indexer, and dashboard.
- [x] Verify Wazuh services and dashboard access.
- [x] Disable the Wazuh package repository to prevent accidental upgrades.
- [ ] Document the server setup with reviewed screenshots.
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
- Accurate timestamps help correlate events during investigations.
- Wazuh uses separate components for event analysis, indexing,
  and dashboard access.
- Running services and successful dashboard access verify the
  initial installation; endpoint monitoring still needs to be tested.

## Investigation findings
No controlled investigation scenarios have been completed yet.
Initial dashboard alert counts have not been investigated and
are not being presented as confirmed security incidents.
