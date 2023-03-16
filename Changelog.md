#  Changelog

#### OpenCore 0.6.7
- Updated to OpenCore 0.6.7
- Updated to Acidanthera March kext(s)
- Fixed SD Card Reader to work after wake from sleep
- Fixed SD Card volumes to show correct SD icon instead of USB.
- Complete ACPI cleanup and Re-write
- Added YogaSMC to read & control Fan, LEDs and full keyboard map and Fn shortcuts GUI
- Enabled OpenCanopy support
- Added Modern OpenCanopy Design introduced into Big Sur
- Fixed VoodooRMI to work with standard touchpads
- Fixed Ethernet causing wakes and now no instant wake patches needed
- Added latest AirportItlwmkexts and IntelBluetooth kexts
- Added SecureBoot support
- Added Audio boot chime during startup
- Many other changes that i may have forgot to list (refer to commits)

#### OpenCore 0.6.0
- Updated to OpenCore 0.6.0
- Updated to Acidanthera August kext(s)
- Removed `SSDT-SMBUS` in favor of **VodooSMBus.kext**
- Removed *VoodooPS2TrackPad.kext*, *VoodooPS2Mouse.kext*, *VoodooInput.kext* plugin kexts in VoodooPS2 loading in favor of **VoodooRMI.kext**
- Added **VoodooSMBUS.kext** to load SMBus capabilities of Intel I/O Controller Hubs (ICH), also called i801 SMBus
- Added *VoodooRMI* as default TouchPad kext
- Removed Touchpad configuration from `SSDT-KBD` (now native on VoodooRMI)
- Updated `SSDT-PNLF` to only include Broadwell/Haswell architecture
- Updated `SSDT-KBD` with *Fn+Esc* key support on ThinkPad Assistant and re-arranged the `Methods` by Keyboard order
- Updated `SSDT-KBD` to use `Switch` instead of nested `If` for cleaner and less complicated patches and renamed the calls for MicMute, CapsLock and FnLock LED(s)
- Fixed accidental kext  `Linking Problems` regression introduced by me on OpenCore 0.5.9 EFI update where Bluetooth wouldn't work and system would Kernel Panic
