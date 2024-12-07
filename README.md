# OpenCore Config EFI for Z690-A Pro Wifi

**Latest working macOS**: 15.1.1 (works on Sonoma as well).

**SMBIOS**: iMacPro1,1 (MacPro7,1 works alebit less performant)

**OpenCore**: 1.0.3

> [!WARNING]
> You do this on your own risk, I will not be responsible for what happens to your machine if you don't follow proper instructions (i.e getting banned because you don't change SMBIOS info). Troubleshooting can be done if you supply proper information and ways to reproduce the issues and submit it as an issue on this repo.
<p align="center">
  <img width="auto" height="500px" src="https://github.com/user-attachments/assets/5534e279-92a0-4bf9-95d0-87d7b73a319b">
</p>

---

## Get it running

1. Download latest BIOS version.
2. Disable CfgLock, Secure Boot, VT-D in BIOS (Check wakeup-event by bios then choose usb for usb wakeups).
3. Create your recovery using OpenCorePkg.
4. Download the EFI, extract it and make sure to pick the "EFI".
5. Format your USB as FAT32, make sure that the EFI folder and recovery files is in the root of your USB.
6. Install MacOS.
7. Change RAM information (PI > Memory) and generate SMBIOS using [OCAT](https://github.com/ic005k/OCAuxiliaryTools) on the USB.
8. Mount your EFI using [MountEFI.command](https://github.com/corpnewt/MountEFI)
9. Copy the EFI to your mounted EFI partition.
10. Turn ShowPicker to False (if you don't want a picker at start-up) in [OCAT](https://github.com/ic005k/OCAuxiliaryTools).
11. Wifi for Sequoia: Turn on Itlwm and download heliport
12. Wifi for Sonoma: Download AirportItlwm
13. Troubleshoot for any issues (shouldn't be any but just in case).
> [!NOTE]
> Enable HiDPI Display settings by running `sudo defaults write /Library/Preferences/com.apple.windowserver.plist DisplayResolutionEnabled -bool true` and rebooting the PC

Some useful [tips and tricks](https://github.com/5T33Z0/OC-Little-Translated/tree/main/A_Config_Tips_and_Tricks) and the full [OpenCore Documentation](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html)

## Portmapping
I've done the mapping for Z690-A Pro Wifi using [USBToolBox](https://github.com/USBToolBox/tool), you can make your own if an USB port does not work.

## Todos
- [ ] Check for wakeups during sleep.
- [ ] Check multiboot compatibility.

## Kexts Used (for maintanence)

- Lilu
- VirtualSMC
- NootRX
- AppleALC
- SMCSuperIO/SMCProcessor
- CpuTopologyRebuild
- CpuTscSync
- ForgedInvariant
- RestrictEvents
- AppleIGC
- Itlwm/AirportItlwm
- IntelBTPatcher (Sonoma)
- IntelBluetoothFirmware (Sonoma)
- BluetoolFixup (Sonoma)
- NVMEFix
- USBToolBox
- UTBMap
- HibernationFixup

### Functionality
| Component    | Status |
|:---------:|:---:|
| Wifi      | ✅ (Disabled by default as I don't use it) |
| Bluetooth | ✅ |
| Ethernet  | ✅ |
| iGPU      | (Not tested) |
| dGPU      | ✅ |
| NVME      | ✅ |
| DRM       | 🚫 |
| ACPI      | ✅ |

### Hardware

| Component    | Variant                   | Link                                                                                                                                         |
|:------------:|:-------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------:|
| Mainboard    | MSI Z690-A Pro Wifi DDR4  | [Link](https://www.msi.com/Motherboard/PRO-Z690-A-WIFI-DDR4)                                                                                 |
| Processor    | Intel Core i5 12400F      | [Link](https://ark.intel.com/content/www/us/en/ark/products/134587/intel-core-i512400f-processor-18m-cache-up-to-4-40-ghz.html)              |
| Audio        | ALC897                    |                                                                                                                                              |
| DDR4 RAM     | HyperX Fury Beast 32GB    | [Link](https://www.kingston.com/datasheets/KF436C16RB1A_16.pdf)                                                                              |
| NVMe SSD     | WD_Black SN850 NVME       |                                                                                                                                              |
| Graphics     | AMD Radeon RX 6700XT      | [Link](https://www.amd.com/en/products/graphics/amd-radeon-rx-6700-xt)                                                                       |
| WiFi / BT    | Intel® Wi-Fi 6E           | [Link](https://www.intel.com/content/www/us/en/products/sku/130293/intel-wifi-6-ax201-gig/specifications.html)                               |
| Lan / Ethernet| Intel® I225-V            |                                                                                                                                              |

## Credits
- OpenCore Team for OpenCore
- Kext Maintainers for driver functionalities
- [Rursache](https://github.com/rursache) for proper documentation standards
