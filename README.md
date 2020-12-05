# Dell-Optiplex-7040-OpenCore
OpenCore Configuration for Dell Optiplex 7040.
Should also work with 7050 and 7060 by replacing the ACPI files with the correct ones for Kaby Lake & Coffee Lake.

This is assuming you're using a stock model with just the iGPU, and either a SATA HDD, M.2 SSD or both. If using a dedicated GPU, be sure to add the appropriate tweaks needed.

F2 Settings (before installing):
- Uncheck "Enable Legacy Option ROMS"
- Disable Serial Port
- SATA Operation: AHCI
- Secure Boot Enable: Disabled
- Intel SGX Enable: Disabled
- HyperThread control: Enabled (this will only show for Core i7 users)
- (6700K only) Fan Control Override: Check - this will improve thermals

How to install (This is assuming you have a macOS computer available, whether a real Mac or an existing Hackintosh):
- Create a macOS install USB.
- Use Clover Configurator to mount the EFI partition of the USB stick you just made
- Drag and drop the EFI folder into the root folder of the EFI partition
- Press F12 upon seeing dell logo and select your USB stick.

Post-Installation:
- Open Clover Configurator to mount the EFI partition of BOTH your USB stick and the primary storage device where macOS is installed.
- Drag and drop the EFI folder from your USB stick into the root folder of your EFI partition of your primary storage device
- Unmount both EFI partitions
- Reboot and enter F2 menu to clear the boot list from the Boot Sequence menu
- F12 again and boot to your primary storage.

*DO NOT USE CLOVER CONFIGURATOR FOR ANYTHING ELSE, WE ONLY USE IT FOR MOUNTING THE EFI PARTITION!*

