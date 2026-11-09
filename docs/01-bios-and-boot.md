# BIOS and Boot Configuration

## Hardware and firmware

- The PC uses UEFI firmware.
- The exact motherboard model and BIOS version were not recorded.
- The firmware setup key is therefore not documented.

## Power-loss behavior

After disconnecting and reconnecting power, or after a power outage, the firmware displayed:

    Optimize Settings?

The system paused and required user input before continuing to boot.

## Possible CMOS battery issue

A weak CMOS battery was considered a possible cause because of the machine's age.

This diagnosis has not been confirmed:

- The CMOS battery has not yet been replaced.
- No explicit CMOS battery error was recorded.
- Ubuntu system time synchronization does not establish battery health.

## Suggested recovery procedure

1. Shut down the PC and disconnect power.
2. If battery failure is suspected, inspect the motherboard battery.
3. Replace it with a compatible CR2032 3V lithium battery if confirmed appropriate.
4. Enter firmware setup and verify the date and time.
5. Check the power-recovery option, commonly named `Restore AC Power Loss`, `AC Back` or similar.
6. If unattended recovery is required, select `Power On` where supported.
7. Verify the UEFI boot order and preserve the existing Windows boot entry.
8. Save settings and test a controlled power cycle.

## Important precautions

- Firmware menu names vary by motherboard.
- Replacing the CMOS battery may reset firmware settings.
- Recheck UEFI boot settings after replacement.
- Do not assume the battery is faulty until verified.

## Current status

The power-recovery issue remains unresolved. The battery has not been replaced, and no successful unattended power-recovery test has been recorded.
