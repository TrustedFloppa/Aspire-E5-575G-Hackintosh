# Adding The Base OpenCore Files
To setup OpenCore’s folder structure, you’ll want to grab the EFI folder found in OpenCorePkg's releases 
Note that they will be under either the IA32 or X64 folders, the former for 32-bit Firmwares and the latter for 64-bit Firmwares:
![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/ia32-x64.aa5dccd9.png)

And once downloaded, place the EFI folder(from OpenCorePkg) on the root of your EFI partition:
![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/efi-moved.87262fda.png)

# Now lets open up our EFI folder and see what's inside:
![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/base-efi.7500e22d.png)

**Now something you'll notice is that it comes with a bunch of files in Drivers and Tools folder, we don't want most of these:**
**Keep the following from Drivers**(if applicable):
OpenRuntime.efi	Required for proper operation
> OpenPartitionDxe.efi	Required to boot macOS 10.7-10.9 recovery

A cleaned up EFI:
![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/clean-efi.10fb2a26.png)

Reminder:

SSDTs and custom DSDTs(.aml) go in ACPI folder
Kexts(.kext) go in Kexts folder
Firmware drivers(.efi) go in the Drivers folder

# Now with all this done, head to [Gathering Files](https://www.google.com) to get the needed kexts and firmware drivers
