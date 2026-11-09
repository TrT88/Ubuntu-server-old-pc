# Ubuntu Server on Legacy PC

An anonymized technical build log documenting the installation and configuration of Ubuntu Server on an older Intel-based PC.

## Hardware

| Component | Specification |
|---|---|
| CPU | Intel Pentium G2030 @ 3.00 GHz |
| CPU cores / threads | 2 / 2 |
| RAM | 8 GB |
| Architecture | x86-64 |
| Firmware | UEFI |
| Storage | HDD |

The machine originally had Windows installed. The Windows system partition and EFI System Partition were preserved during the Ubuntu installation process.

## Ubuntu installation history

Several Ubuntu Server releases were tested:

- Ubuntu Server 26
- Ubuntu Server 24.04.5
- Ubuntu Server 24.04.4
- Ubuntu Server 22 — the release that worked best on this machine.

The exact ISO build numbers and detailed failure logs were not retained. No specific failure cause is claimed.

## Documentation

- [BIOS and Boot](docs/01-bios-and-boot.md)
- [Disk and Partition Safety](docs/03-disk-and-partition-safety.md)
- [Network and Remote Access](docs/04-network-and-remote-access.md)
- [UEFI and GRUB](docs/05-uefi-and-grub.md)

## Safety notes

- Back up important data before changing partitions.
- Inspect disks with read-only commands before any destructive operation.
- Never assume a Windows drive letter maps directly to a particular Linux device.
- Preserve the existing EFI System Partition unless there is a verified reason to change it.
- Anonymize hostnames, usernames, IP addresses, Wi-Fi details and credentials before publishing logs.

## Disclaimer

This documentation describes one specific older-PC setup. Hardware compatibility and installation results may differ on other machines.
