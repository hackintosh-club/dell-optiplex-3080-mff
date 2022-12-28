
## Dell OptiPlex 3080 Micro (3080MFF) Hackintosh OpenCore EFI


### [简体中文](README.zh_CN.md)



### OpenCore

[OpenCore 0.8.7](https://github.com/acidanthera/OpenCorePkg)



### Spec

- BIOS: 2.16.0
- Chipset: DELL B460
- CPU: Intel 10th i5-10500T
- Memo: SK hynix 16GB(2x8GB) DDR4 3200 Mhz
- iGPU: Intel UHD Graphic 630
- 声卡: Realtek ALC3246(ALC256)
- SSD: Kioxia 512G (KBG40ZNS) m.2 2230
- LAN: Realtek RTL8111HSD-CG
- WLAN: Intel AX200 / BCM94360CS2
- PSU: DELL 65w



### BIOS

```
System Configuration
  |-- SATA Operaition: AHCI

Video
  |-- Primary Display: Intel HD Graphics

Security
  |-- PTT Security/PTT On: Disabled

Secure Boot
  |-- Secure Boot Enable: Disabled

PSecure Boot
  |-- Secure Boot Mode: Audit Mode

Intel Software Guard Extensions
  |-- Intel SGX Enable: Disabled

PowerManagement
  |-- Deep Sleep Control: Disabled
  |-- USB Wake Support:   Disabled
  |-- Wake on LAN/WLAN:   Lan only
  |-- Block Sleep:        YES

POST Behavior
  |-- Fastboot: Minimal

Virtualization Support
  |-- VT For Direct I/O: Disabled
```



### Notice

- Use [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) build your own SMBIOS
- Use [RU.efi](RU.efi) Unlock `CFG LOCK` , Change `DVMT = 64MB`

Option   | UEFI Variable Name | Address | Default | Replace
---------|--------------------|---------|---------|---------
CFG LOCK | CPUSetup           | 0x3E    | 0x1     | 0x0
DVMT     | SaSetup            | 0xF5    | 0x0     | 0x2

- Unlock CFG LOCK Address:0x3E 01 (Enabled) Replace 00（Disabled）
![cpusetup.png](Screenshot/cpusetup.png)

- Change DVMT Address:0xF5 00（Default） Replace 02（64MB）
![sasetup.png](Screenshot/sasetup.png)



### Kexts

- [Lilu.kext 1.6.2](https://github.com/acidanthera/Lilu)
- [SMCProcessor.kext 1.3.0](https://github.com/acidanthera/VirtualSMC)
- [SMCSuperIO.kext 1.3.0](https://github.com/acidanthera/VirtualSMC)
- [SMCDellSensors.kext 1.3.0](https://github.com/acidanthera/VirtualSMC)
- [VirtualSMC.kext 1.3.0](https://github.com/acidanthera/VirtualSMC)
- [WhateverGreen.kext 1.6.2](https://github.com/acidanthera/WhateverGreen)
- [NVMeFix.kext 1.1.0](https://github.com/acidanthera/NVMeFix)
- [AppleALC.kext 1.7.7](https://github.com/acidanthera/AppleALC)
- [RealtekRTL8111.kext 2.4.2](https://github.com/Mieze/RTL8111_driver_for_OS_X)
- [USBMap.kext v1.0.0](https://github.com/corpnewt/USBMap)
- [XHCI-unsupported.kext v0.9.2](https://github.com/hackintosh-efi/XHCI-unsupported)



### Tools

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) AKA OCC.
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) Generate SMBIOS.
- [MountEFI](https://github.com/corpnewt/MountEFI) Mount EFI partition.
- [EFI Agent](https://github.com/headkaze/EFI-Agent) Better EFI partition mount App.
- [gibMacOS](https://github.com/corpnewt/gibMacOS) Build your own MacOS image.
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist editor.
