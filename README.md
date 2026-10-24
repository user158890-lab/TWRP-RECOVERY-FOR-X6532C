# TWRP Recovery for Infinix Smart 9 HD (X6532C)

This repository contains the recovery fstab and custom recovery  for the Infinix Smart 9 HD, model X6532C.

## Installation image

The recovery image belongs in the `vendor_boot` partition, not the `recovery` partition.write it only to the slot that is currently active. 

Before writing an image, confirm all of the following:

1. The image is built for X6532C (INFINIX SMART 9 HD) 
2. The image size matches the device vendor_boot partition.
3. The active slot is known.

## FEATURES

- No data wipe is required to use this recovery.
- Works with encrypted devices without removing existing encryption.
- Supports flashing, backup, installing ZIP and image files and all other custom recovery features. 
- Tested on a real Infinix Smart 9 HD X6532C device.

## TIPS FOR FLASHING 

USING FASTBOOT : fastboot flash vendor_boot_a/b(recovery.img)

USING ROOT : IMG=/sdcard/Download/TWRP_X6532C.img
SLOT=$(getprop ro.boot.slot_suffix); dd if=$IMG of=/dev/block/by-name/vendor_boot$SLOT bs=4M conv=fsync && sync
