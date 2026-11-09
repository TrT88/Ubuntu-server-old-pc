# Disk and Partition Safety

## Original disk layout

The PC originally contained:

- A Windows system partition (C:), approximately 97.54 GB.
- A data partition (D:), approximately 135.23 GB.
- An EFI System Partition, approximately 100 MB.

The data on D: was backed up and removed before preparing that space for Ubuntu.

## Partitions to preserve

- Preserve the Windows system partition.
- Preserve the existing EFI System Partition.
- Do not format or delete partitions based only on their apparent size or position.

## Identify disks before installation

Run these read-only inspection commands on Ubuntu:

    lsblk -o NAME,SIZE,FSTYPE,TYPE,MOUNTPOINTS
    sudo fdisk -l
    sudo parted -l

Review the output carefully before selecting any disk or partition.

## Important precautions

1. Back up important files before modifying the partition layout.
2. Never assume Windows drive D: corresponds to a particular Linux device such as `/dev/sda`.
3. Verify device names, sizes, filesystems and partition contents.
4. Stop if the target disk or partition is uncertain.
5. Do not format the EFI System Partition as part of routine Ubuntu installation.

## Scope

This document records the original layout and safety principles. Exact Linux device mappings were not established and are intentionally omitted.
