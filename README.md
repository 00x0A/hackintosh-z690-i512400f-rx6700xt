# OpenCore EFI for Z690-A Pro Wifi

EFI for OpenCore based on Z690-A Pro Wifi, i5-12400F CPU and RX 6700 XT GPU.
<p align="center">
  <img width="auto" height="500px" src="https://github.com/user-attachments/assets/5534e279-92a0-4bf9-95d0-87d7b73a319b">
</p>


---
# Disclaimer
I will not be responsible for what happens to your machine if you don't follow proper instructions (i.e getting banned because you don't change SMBIOS info)

### Information 

- MacOS: [Sequoia](https://www.apple.com/macos/macos-sequoia/)
- Bootloader: OpenCore 1.0.2
- SMBIOS: iMacPro1,1 (MacPro7,1 works but with less performance)
- Change RAM config according to your specs in PI > Memory [OCAT](https://github.com/ic005k/OCAuxiliaryTools)
- Generate SMBIOS for your own setup, don't use the existing one! 

### Functionality
| Component    | Status |
|:---------:|:---:|
| Wifi      | 🚫 | (Sequoia, works on Sonoma)
| Bluetooth | 🚫 | (Sequoia, works on Sonoma)
| Ethernet  | ✅ |
| dGPU      | ✅ |
| NVME      | ✅ |
| DRM       | 🚫 |
| Wakeup/Restart/Power Off| ✅ |

### Hardware

| Component    | Variant                   | Link                                                                                                                                         |
|:------------:|:-------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------:|
| Mainboard    | MSI Z690-A Pro Wifi DDR4  | [MSI](https://www.msi.com/Motherboard/PRO-Z690-A-WIFI-DDR4)                                                                                  |
| Processor    | Intel Core i5 12400F      | [Intel i5 12400F](https://ark.intel.com/content/www/us/en/ark/products/134587/intel-core-i512400f-processor-18m-cache-up-to-4-40-ghz.html)   |
| Audio        | ALC897                    |                                                                                                                                              |
| DDR4 RAM     | HyperX Fury Beast 32GB    | [Kingston](https://www.kingston.com/datasheets/KF436C16RB1A_16.pdf)                                                                          |
| NVMe SSD     | WD_Black SN850 NVME       |                                                                                                                                              |
| Graphics     | AMD Radeon RX 6700XT      | [AMD Radeon RX 6700XT](https://www.amd.com/en/products/graphics/amd-radeon-rx-6700-xt)                                                       |
| WiFi / BT    | Intel® Wi-Fi 6E           | [Intel Wi-Fi 6E](https://www.intel.com/content/www/us/en/products/sku/130293/intel-wifi-6-ax201-gig/specifications.html)                     |
| Lan / Ethernet| Intel® I225-V            |                                                                                                                                              |
