

# Acer A515 51G 51D3 Hackintosh

<p align="center">
  <img src="https://i.imgur.com/O9WG5Np.png" alt="Specs">
</p>


## What's Working...
 - [x] Audio & headphone jack
 - [x] CPU Speedstep (XCPM)
 - [x] iGPU with disabled dGPU
 - [x] Fully Functional QE/CI Enabled Graphics
 - [x] Battery Management
 - [x] Ethernet
 - [x] HDMI + Audio
 - [x] Smart Touchpad + Gestures (using I2C)
 - [x] WebCam
 - [x] Usb 3.0 + Type C
 - [x] WiFi
 - [x] Native hotkey support with Fn keys

## What's not Working
 - [ ] Sleep + Wake
 - [ ] Brightness + Brightness Keys

## Installation

###  Basic Installation

- Create a Bootable USB for MacOS by using [USB Installation Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install.html)
- Copy **ALL** the Contains of this Repo inside the EFI partition of USB

### Post Installation

- Copy **ALL** the Contains of this Repo inside the EFI partition of Hard Drive where you installed the OS
---
### Laptop configuration


- **Audio** : The Sound Card is `Realtek ALC255`, which is driven by `AppleALC` on `layout-id 30`. It supported using `AppleALC.kext`

- **CPU** : The CPU model is `i5-8250U` and XCPM power management is natively supported.

- **Graphics** : The iGPU is `Intel UHD Graphics 620`, and its enabled using `Ig-Platform-id=0x191E0000`.

- **Battery** : Battery Management using `SMCBatteryManager.kext`.

- **Touchpad** : Elan Touchpad. Supported using `VoodooI2C.kext` + `VoodooI2CHID.kext`

- **Keyboard** : PS2. Supported using `VoodooPS2Controller.kext`

- **USBs** : Custom generated. Supported using `USBToolBox.kext` + `UTBMap.kext`

- **Ethernet** : Gigabit Ethernet using `RealtekRTL8111.kext`.

- **HDMI** : Working using `WhateverGreen.kext`.

- **Wi-Fi** : Stock WiFi Card is `Intel Wireless AC 3168`. It supported using `AirportItlwm.kext`

- **Bluetooth** : Stock `Intel Wireless AC 3168`. Supported using `IntelBluetoothFirmware.kext` + `IntelBTPatcher.kext` + `BlueToolFixup.kext`

## Credits

- **Special Thanks** to [zqlovezone](https://github.com/zqlovezone/ACER-TX520-Hackintosh-Opencore) from where I've forked it.
