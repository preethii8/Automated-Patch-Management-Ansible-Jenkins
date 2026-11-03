# Automated Patch Management Using Ansible and Jenkins

## Overview
Automated security patch management for Red Hat Enterprise Linux 9 using Ansible and Jenkins.

## Technologies
- Red Hat Enterprise Linux 9
- Ansible
- Jenkins
- SSH
- DNF
- Oracle VirtualBox

## Architecture
Jenkins (LINUX1) → Ansible → SSH → RHEL9 (LINUX2)

## Features
- Pre-patching health checks
- Root and boot partition disk-space validation
- Automated security updates
- Conditional server reboot
- Post-patching kernel, disk, and memory verification

## Execution Results
- Jenkins Pipeline: SUCCESS
- Security updates: Installed
- Automatic reboot: Successful
- Kernel before: 5.14.0-687.61.1.el9_8.x86_64
- Kernel after: 5.14.0-687.65.1.el9_8.x86_64
- Failed tasks: 0

## Files
- automated_patching.yml — Main patching playbook
- health_check.yml — Server health checks
- patch_check.yml — Patch checking
- patch_install.yml — Patch installation
- Jenkinsfile — Jenkins automation pipeline
- inventory.ini.example — Example inventory

## Security
Use SSH key authentication and appropriately restricted privilege escalation.
Never commit credentials or private SSH keys.
