
## Dell OptiPlex 3080 Micro (3080MFF) 黑苹果 OpenCore EFI


### [English](README.md)



### OpenCore

[OpenCore 0.8.7](https://github.com/acidanthera/OpenCorePkg)



### 机器配置

- 型号: Dell OptiPlex 3080 MFF
- BIOS: 2.16.0
- 芯片组: B460
- CPU: Intel 10代 i5-10500T
- 内存: 海力士 16GB(8GBx2) 3200 Mhz
- 显卡: Intel UHD630
- 声卡: Realtek ALC3246(ALC256)
- SSD: 铠侠 Kioxia 512G (KBG40ZNS) m.2 2230
- 网卡: Realtek RTL8111HSD-CG
- 无线网卡: Wireless network card



### BIOS设置

```
System Configuration
  |-- SATA Operaition: AHCI

Video
  |-- Primary Display: Intel HD Graphics

Intel Software Guard Extension
  |-- Intel SGX Enable: Disabled

Performance
  |-- Intel TurboBoost: YES

PowerManagement
  |-- Deep Sleep Control: Disabled
  |-- Block Sleep: YES
```



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



### 工具

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) 即 `OCC`。
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) 三码生成工具。
- [MountEFI](https://github.com/corpnewt/MountEFI) EFI 分区挂载工具。
- [EFI Agent](https://github.com/headkaze/EFI-Agent) 更方便的EFI分区挂载工具。
- [gibMacOS](https://github.com/corpnewt/gibMacOS) macOS 官方镜像下载工具。
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist 编辑器。
