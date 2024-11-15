# OpenCore 1.0.2 - macOS 15 (Sequoia)

OpenCore configuration for booting on an HP Pavillion 14 laptop.
Still in progress, but you should be able to boot and install.

Note: SSDT files are built for my system, thus it may not work for other systems. I strongly recommend that you build it specific to your device.

## Device Info

- Model: HP Pavillion 14 - ce2003nx
- CPU: Intel i7 8565u
- iGPU: Intel UHD 620
- dGPU: Nvidia MX250 (disabled)
- RAM: 8 GB DDR4
- SSD: LITEON CV8-8E128-HP
- Audio: Realtek ALC295
- Ethernet: Realtek RTL8111

## BIOS Settings

- CSM: Disabled
- Intel SGX: Disabled
- Secure Boot: Disabled
- SATA Devices: AHCI mode

## Getting Started

1. Clone the repository.
1. Fill up `config.plist > PlatformInfo` using `MacbookPro15,2`.
1. Obtain a copy of recovery.
1. Wait for boot to finish, should take a while as included OpenCore is for debug.
1. Install the OS.
1. Boot into `macOS Installer` until it is done.
   1. If you encounter a boot loop, try setting `SecureBootModel` to `Disabled`.
   2. After finishing the install, you can set it back to `Default`.
1. Boot into the OS.

## What's working

- Ethernet
- iGPU Acceleration
- Brightness
- USB
- Audio
- Sleep

## What's not working

- WiFi
- Webcam (Black Screen)

## Untested

- Siri
- iMessage
- Microphone
