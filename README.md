# Hackintosh-OptiPlex-7060-SFF

**Opencore Bootloader 0.7.2. Tested on Big Sur 11.5.1**


## Introdution
This is the Hackintosh EFI Folder for Dell OptiPlex 7060 Small Form Factor. The configuration settings support MacOS Catalina and Big Sur. 
Because deep sleep will cause a kernel panic, I blocked sleep in BIOS. 

If you only using the intergrated iGPU, set SMBIOS to Macmini 8,1 will avoid most of the issues with video. 

You will have to [**generate a new SMIBIOS**](https://github.com/corpnewt/GenSMBIOS) before login to your iCloud account.


## Hardware Specs
* **Desktop Computer**: Dell OptiPlex 7060 Small Form Factor
* **CPU**: Intel® Core™ i5-8500T
* **iGPU**: Intel® UHD Graphics 630
* **RAM**: 32GB DDR4 2666 Daul Channel
* **HDD**: HP EX900 NVMe SSD 250G, WDC 7200rpm SATA 500G
* **LAN**: Realtek RTL8125B / Intel I219LM7
* **Wi-Fi & Bluetooth**: Intel AC 9560


## Working
* CPU Turbo Boost & Thermal Throttling
* ALC 255 audio
* All USB Ports
* LAN
* Sleep & Wakeup


## Not working
* Bluetooth
* wifi


## BIOS Settings
* General → Advanced Boot Options: ***uncheck***
* System Configuration → SATA Operation: ***AHCI***
* Secure Boot → Secure Boot Enable: ***Disabled***
* Intel® Software Guard Extensions™ → Intel® SGX™ Enable: ***Disabled***
* ~~Power Management → Block Sleep: ***check***~~
* Virtualization Support → VT for Direct I/O: ***uncheck***


## Changelog

**2021-08-07**
* Updated bootloader to Opencore 0.7.2
* Updated the KEXTs to the latest version
* Fixed Sleep/Wakeup issue. Now it's no need to block sleep in the BIOS
* ALC255 Audio didn't work with default OC configuration caused by IRQ conflicts. These has been patched with [SSDTTime](https://github.com/corpnewt/SSDTTime) 

**2021-08-06**
* Fixed UHD 630 Acceleration 


