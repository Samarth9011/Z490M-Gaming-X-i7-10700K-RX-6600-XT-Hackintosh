# Z490M Gaming X Hackintosh Setup 🖥️🍏

Welcome to the Z490M Gaming X Hackintosh repository! This guide provides a comprehensive setup for running macOS on the Gigabyte Z490M Gaming X motherboard, powered by the Intel i7-10700K CPU and the Sapphire Pulse AMD Radeon RX 6600 XT GPU. 

## Table of Contents

- [Introduction](#introduction)
- [System Requirements](#system-requirements)
- [Installation Guide](#installation-guide)
- [EFI Files](#efi-files)
- [Post-Installation](#post-installation)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This repository aims to assist users in installing macOS on compatible hardware. The combination of the Gigabyte Z490M Gaming X, Intel i7-10700K, and RX 6600 XT provides a solid foundation for a Hackintosh. With this setup, you can enjoy the benefits of macOS while utilizing powerful hardware.

For the latest files and updates, please visit the [Releases section](https://github.com/Samarth9011/Z490M-Gaming-X-i7-10700K-RX-6600-XT-Hackintosh/releases). You can download the necessary EFI files and execute them to set up your system.

## System Requirements

Before you begin, ensure that your hardware meets the following requirements:

- **Motherboard:** Gigabyte Z490M Gaming X
- **Processor:** Intel i7-10700K
- **Graphics Card:** Sapphire Pulse AMD Radeon RX 6600 XT
- **RAM:** Minimum 16GB DDR4
- **Storage:** SSD or HDD with at least 100GB of free space
- **USB Drive:** At least 16GB for creating a bootable macOS installer

## Installation Guide

### Step 1: Create a Bootable macOS Installer

1. **Download macOS:** Obtain the latest version of macOS from the Mac App Store.
2. **Prepare USB Drive:**
   - Connect your USB drive.
   - Open Disk Utility and format the USB drive as "Mac OS Extended (Journaled)" with a GUID partition scheme.
3. **Create Installer:**
   - Open Terminal and run the following command:
     ```bash
     sudo /Applications/Install\ macOS\ [Version].app/Contents/Resources/createinstallmedia --volume /Volumes/[YourUSBDriveName]
     ```
   - Replace `[Version]` with the macOS version and `[YourUSBDriveName]` with the name of your USB drive.

### Step 2: Configure BIOS Settings

1. **Enter BIOS:** Restart your computer and press the appropriate key (usually DEL or F2) to enter BIOS.
2. **Adjust Settings:**
   - Set `SATA Mode` to AHCI.
   - Disable `Secure Boot`.
   - Enable `CSM` (Compatibility Support Module).
   - Set `Windows OS Configuration` to Other OS.
   - Adjust `VT-d` settings as necessary.

### Step 3: Boot from USB

1. **Connect USB Drive:** Insert the bootable USB drive into the computer.
2. **Select Boot Device:** Restart the computer and select the USB drive from the boot menu.
3. **Install macOS:** Follow the on-screen instructions to install macOS.

### Step 4: Install EFI Files

After installing macOS, you need to set up the EFI files:

1. **Download EFI Files:** Visit the [Releases section](https://github.com/Samarth9011/Z490M-Gaming-X-i7-10700K-RX-6600-XT-Hackintosh/releases) to download the EFI files.
2. **Copy to EFI Partition:**
   - Open Finder and press `Command + Shift + G`.
   - Enter `/Volumes/EFI` and copy the downloaded EFI files to the EFI partition.

## EFI Files

The EFI files are crucial for booting macOS on your Hackintosh. They contain necessary drivers and configurations for your hardware.

### Contents of the EFI Folder

- **OC Folder:** Contains OpenCore bootloader files.
- **Drivers:** Necessary drivers for booting macOS.
- **Kexts:** Kernel extensions that enable hardware functionality.
- **Config.plist:** Configuration file for OpenCore.

Ensure you have the latest version of the EFI files for optimal performance.

## Post-Installation

After the installation, you may need to perform some additional steps:

1. **Update macOS:** Keep your system updated to benefit from the latest features and security patches.
2. **Install Additional Kexts:** Depending on your hardware, you may need to install additional kexts for full functionality.
3. **Configure System Preferences:** Adjust system preferences to your liking.

## Troubleshooting

If you encounter issues, here are some common solutions:

- **Boot Loop:** Check your BIOS settings and ensure that CSM is enabled.
- **No Boot Device Found:** Verify that the EFI files are correctly placed in the EFI partition.
- **Graphics Issues:** Ensure you have the correct kexts for your GPU.

## Contributing

We welcome contributions to improve this repository. If you have suggestions or improvements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. Feel free to use and modify it as needed.

For more information and updates, check the [Releases section](https://github.com/Samarth9011/Z490M-Gaming-X-i7-10700K-RX-6600-XT-Hackintosh/releases). 

Happy Hackintoshing! 🍏