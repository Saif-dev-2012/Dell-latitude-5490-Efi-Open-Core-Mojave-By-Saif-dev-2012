Hackintosh EFI - Dell Latitude 5490 / Kaby Lake + OC 0.8.8

EFI for macOS Mojave 10.14.6 on Dell Latitude 5490 with Intel 7th Gen CPU

Specs

Component Details

Model
Dell Latitude 5490

CPU
Intel Core i5 7300U

GPU
Intel HD Graphics 620

RAM
16GB DDR4 2133mhz ( 2 x 8 gb ram)

Storage
512GB Kingston SSD Sata III

WiFi/BT
Intel Dual Band Wireless-AC 8265

Audio
Realtek ALC

LAN
Atheros E2200 + Realtek RTL8111

macOS
Mojave 10.14.6

Bootloader
OpenCore 0.8.8

SMBIOS
MacBookPro14,1



What Works
[v]  Graphics Acceleration QE/CI - WhateverGreen
[v]  Audio - Internal Speakers + Jack - AppleALC
[v]  Bluetooth - IntelBTPatcher
[v]  LAN - Atheros E2200 + Realtek RTL8111
[v]  USB Ports - USBInjectAll
[v]  Battery Status - SMCBatteryManager
[v]  Sleep/Wake
[v]  Brightness Keys - BrightnessKeys.kext
[v]  Trackpad + Keyboard - VoodooPS2 + VoodooI2C
[v]  NVMe - NVMeFix for NVMe disks
[v]  EC - ECEnabler

What Doesn't Work
• HDMI Audio - Not tested yet
• Fingerprint Reader - Not supported on macOS
• Wifi - No Wifi kext added - Using USB Tethering

Kexts Used - v0.8.8 Open Core:
• Lilu.kext V1.7.2
• VirtualSMC.kext V1.3.8 + SMCBatteryManager + SMCLightSensor + SMCProcessor
• WhateverGreen.kext V1.6.0
• AppleALC.kext V1.8.6

Networking:
• AtherosE2200Ethernet.kext V2.4.0
• RealtekRTL8111.kext V2.4.2
• IntelBluetoothFirmware.kext V2.4.0
• IntelBTPatcher.kext V2.4.0
• BlueToolFixup.kext V2.7.1

Laptop + Input:
• VoodooPS2Controller.kext V2.3.8 + Keyboard + Mouse plugins
• VoodooI2C.kext V2.8.1 + VoodooI2CGPIO + VoodooI2CServices + VoodooI2CHID
• BrightnessKeys.kext V1.0.4
• ECEnabler.kext V1.0.6

Other:
• NVMeFix.kext V1.1.4
• USBInjectAll.kext V1.0
• RestrictEvents.kext V1.1.7
• XHCI-unsupported.kext V1.0

Important Notes
1. BT needs the 3 IntelBT kexts above.
2. Dual LAN: Both Atheros and Realtek kexts included. Disable one in config if you only use 1 port.
3. OC Version: Built and tested on OpenCore 0.8.8
4. No Spoofs Used - Native IDs. MacBookPro14,1 SMBIOS
5. Apple recovery files must be from their servers then put it in the root of usb



Disable these before installation
1.Secure boot > disabled
2.Intel SGX > disabled
3.VT-d > disabled
4. Fastboot > through
5. SATA Operation > AHCI not RAID


Installation
1. Generate your own serials with GenSMBIOS 
2. Put it in usb if you are going to flash it for the first time with Mojave dmg and chunklist in the apple recovery folder you get from apple ( not here ) , then install the macOS normally from the recovery , After booting :

1  Mount EFI partition
2. Copy this 'EFI' folder to 'EFI/' and click merge 
3. Remove the apple recovery files only that you moved to The ssd keep EFI , OC , Apple and what is on them
3. Reset NVRAM on first boot:' Spacebar > Reset NVRAM' in OC picker

Credits
• OpenCore Team
• Acidanthera - Lilu, WEG, AppleALC, VirtualSMC
• VoodooI2C Team, VoodooPS2 Team
• Intel WiFi/BT Team - itlwm, IntelBluetoothFirmware
• Dortania Guide

Disclaimer
This EFI is for educational purposes. Use at your own risk. I am not responsible for any damage.
Built by Saif.dev.
