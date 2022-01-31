

# Acer-A515-51G-51D3-Hackintosh

#### Tested with MacOS 12.2

<p align="center">
  <img src="https://i.imgur.com/WHjb8Wg.png" alt="Specs">
</p>


## What's Working...
 - [x] Audio & headphone jack
 - [x] CPU Speedstep (XCPM)
 - [x] iGPU with disabled dGPU
 - [x] Fully Functional QE/CI Enabled Graphics
 - [x] Battery Management
 - [x] ACPI Display brightness with hot keys / slider
 - [x] Ethernet
 - [x] Internal SD card Reader
 - [x] HDMI + Audio
 - [x] Sleep + Wake
 - [x] Smart Touchpad + Gestures (using I2C)
 - [x] WebCam
 - [x] Usb 3.0 + Type C
 - [x] Sleep From Lid
 - [x] WiFi by using HeliPort and itlwm.kext
 - [x] Native hotkey support with Fn keys

<p align="center">
  <img src="https://i.imgur.com/A0cKRrX.png" alt="Benchmarks">
</p>

  - Geekbench Score :
  - - Single-Core Score : 4219 [Link](https://browser.geekbench.com/v4/cpu/13793813).
  - - Multi-Core Score : 14837 [Link](https://browser.geekbench.com/v4/cpu/13793813).
  - - GPU OpenCL Score : 31191 [Link](https://browser.geekbench.com/v4/compute/4258348).

## Installation

###  Basic Installation

- Create a Bootable USB for MacOS by using [USB Installation Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install.html)
- Copy **ALL** the Contains of this Repo inside the EFI partition of USB

### Post Installation

- - Copy **ALL** the Contains of this Repo inside the EFI partition of Hard Drive where you installed the OS
---
### Laptop configuration


- **Audio** : The Sound Card is `Realtek ALC255`, which is driven by `AppleALC` on `layout-id 30`.

- **CPU** : The CPU model is `i5-8250U` and XCPM power management is natively supported.
 - - XCPM and HWP are recommended to work together to reach better power management, by injecting `plugin-type=1` with `SSDT-XCPM`, and using `CPUFriend.kext`.

- **Graphics** : The iGPU is `Intel UHD Graphics 620`, and its enabled using `Ig-Platform-id=0x191E0000`.
- - The discrete dGPU is `NVIDIA GeForce MX150`, and it is disabled because macOS doesn't support optimus technology. Plus battery life is much improved.
- - The colour branding or corrupted color depth is fixed with Intel Skylake spoof and EDID fix.
- - Native brightness hotkey support using `DSDT.aml`.

- **Battery** : Battery Management using `SMCBatteryManager.kext`.

- **Backlight** : Native Brightness control using `SSDT-PNLF.aml`.

- **Ethernet** : Gigabit Ethernet using `RealtekRTL8111.kext`.

- **HDMI** : Working using `WhateverGreen.kext`.

- **Wi-Fi** : Stock WiFi Card is `Intel Wireless AC 3168` 
- - It supported using **OpenIntelWireless** with [heliport](https://github.com/OpenIntelWireless/HeliPort) and [itlwm](https://github.com/OpenIntelWireless/itlwm)

- **Bluetooth** : Stock `Intel Wireless AC 3168` BT will work out-of-the box.
- **SD Card Reader** : Internal SD Card Support using Modified Sinetek's rtsx Driver.

## Credits

- **Special Thanks** to [zqlovezone](https://github.com/zqlovezone/ACER-TX520-Hackintosh-Opencore) from where I've forked it.
