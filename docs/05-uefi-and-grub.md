# UEFI and GRUB Configuration

## UEFI boot order

The recorded firmware boot order was:

1. Ubuntu (`shimx64.efi`)
2. Windows EFI Boot Manager
3. CD/DVD Drive
4. Hard Drive

Ubuntu was already the preferred boot entry.

The Windows boot entry was preserved.

## GRUB configuration

The recorded settings in `/etc/default/grub` included:

    GRUB_DEFAULT=0
    GRUB_TIMEOUT_STYLE=hidden
    GRUB_TIMEOUT=0
    GRUB_CMDLINE_LINUX_DEFAULT=""
    GRUB_CMDLINE_LINUX=""

## Boot menu behavior

The system detected Windows through `os-prober`.

The GRUB configuration provided four menu entries:

1. Ubuntu
2. Advanced options for Ubuntu
3. Windows Boot Manager
4. UEFI Firmware Settings

Although the default timeout was configured as zero, the Windows detection logic changed the menu timeout to 10 seconds.

The system displayed the menu for 10 seconds and then automatically booted Ubuntu.

## Validation

The following validation was completed successfully:

    sudo grub-script-check /boot/grub/grub.cfg

The GRUB environment file existed, and `sudo grub-editenv list` returned no entries.

## Decision

The existing boot behavior was considered acceptable.

No GRUB changes were made. The Windows boot option remains available.

## Safety

- Do not change UEFI boot entries without a clear reason.
- Preserve the Windows EFI boot entry.
- Back up GRUB configuration before making changes.
- Validate generated GRUB configuration before rebooting.
