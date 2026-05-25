# Synology NAS Deployment Runbook (IT Best Practices)

## Overview
This project provides a structured, repeatable runbook for deploying a Synology NAS in a secure, controlled, and production-ready manner.

It covers the full lifecycle from hardware staging to production deployment, including backup configuration and offsite disaster recovery.

---

## Phases

### Office Phase
Pre-deployment staging and validation.

Includes:
- Hardware inspection and inventory
- DSM installation
- Drive verification and health checks

Goal:
Ensure hardware and system readiness before deployment.

---

### Customer Site Phase
Production configuration and service enablement.

Includes:
- Network configuration (static IP)
- RAID-6 / SHR-2 storage setup with Btrfs
- Storage validation and data scrubbing
- Active Backup for Business deployment
- Server backup configuration (Server1 and Server3)
- Hyper Backup to Synology C2 (offsite backup)
- Backup validation and monitoring

Goal:
Deliver a fully operational, protected, and recoverable system.

---

## Backup Architecture

- **Local Backup:** Active Backup for Business (ABB)
- **Offsite Backup:** Hyper Backup → Synology C2
- **Strategy:** Full initial backup + incremental updates
- **Protection Model:** Onsite + Offsite redundancy

---

## Key Components

- RAID-6 (SHR-2) for fault tolerance
- Btrfs filesystem for data integrity
- ABB for centralized image-based backups
- Hyper Backup for disaster recovery

---

## Framework Alignment

- CIS Control 1 – Asset Inventory
- CIS Control 11 – Data Recovery

---

## Outcome

A fully deployed Synology NAS environment with:

- Verified hardware and storage
- Automated server backups
- Offsite disaster recovery capability
- Documented and repeatable deployment procedure

---

## Related Project

The full implementation steps are tracked in the GitHub Project board.
