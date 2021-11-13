# Aspire-E5-575G-Hackintosh
Supported Versions of Mac OS X
# Big Sur (10.16)  Catalina (10.15)  Mojave (10.14)  High Sierra (10.13)  Sierra (10.12)  El Capitan (10.11)  Yosemite (10.10)  Mavericks (10.9)  Mountain Lion (10.8)  Lion (10.7)  Snow Leopard (10.6)



# Method 1 : OpenCore
Download OpenCore From Here
https://github.com/acidanthera/OpenCorePkg/releases/download/0.7.5/OpenCore-0.7.5-RELEASE.zip

# Prerequisites
**[CRUCIAL]** Time and patience.
Don't start working on this if you have deadlines or important work. Hackintoshes are not something you should be relying on as a work machine.
# Making the installer in Windows
While you don't need a fresh install of macOS to use OpenCore, some users prefer having a fresh slate with their boot manager upgrades.

To start you'll need the following:

4GB USB Stick

For USB larger than 16 GB to format in FAT32

macrecovery.py

This will require Python installed

# Downloading macOS
To grab legacy installers is super easy, first grab a copy of OpenCorePkg and head to /Utilities/macrecovery/. Next copy the folder path for the macrecovery folder:
![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/file-path.0aea4278.png)

From here, you'll want to open up a Command Prompt and cd into the macrecovery folder that we copied earlier:

cd Paste_Folder_Path
![alt text](https://cdn.glitch.me/6fd3928f-90f0-4238-b2b3-592896d694fd%2FZrzut%20ekranu%202021-11-12%20223518.png?v=1636752942996)


Now run one of the following depending on what version of macOS you want(Note these scripts rely on Python support, please install if you haven't already):

# Lion (10.7):
python macrecovery.py -b Mac-2E6FAB96566FE58C -m 00000000000F25Y00 download
python macrecovery.py -b Mac-C3EC7CD22292981F -m 00000000000F0HM00 download

# Mountain Lion (10.8):
python macrecovery.py -b Mac-7DF2A3B5E5D671ED -m 00000000000F65100 download

# Mavericks (10.9):
python macrecovery.py -b Mac-F60DEB81FF30ACF6 -m 00000000000FNN100 download

# Yosemite (10.10):
python macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000GDVW00 download

# El Capitan (10.11):
python macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000GQRX00 download

# Sierra (10.12):
python macrecovery.py -b Mac-77F17D7DA9285301 -m 00000000000J0DX00 download

# High Sierra (10.13)
python macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000J80300 download
python macrecovery.py -b Mac-BE088AF8C5EB4FA2 -m 00000000000J80300 download

# Mojave (10.14)
python macrecovery.py -b Mac-7BA5B2DFE22DDD8C -m 00000000000KXPG00 download

# Catalina (10.15)
python macrecovery.py -b Mac-00BE6ED71E35EB86 -m 00000000000000000 download

# Big Sur (11)
python macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download

# CAUTION: With macOS 11.3 and newer, XhciPortLimit is broken resulting in boot loops (opens new window). We advise users either install an older OS(ie. macOS 10.15, Catalina) or find a 11.2.3 or older Big Sur installer
For education purposes, we have a copy provided here: macOS 11.2.1 20D75 Recovery Image
If you've already mapped your USB ports (opens new window)and disabled XhciPortLimit, you can boot macOS 11.3+ without issue


**This will take some time, however once you're finished you should get either BaseSystem or RecoveryImage files:
![alt text](https://cdn.glitch.me/6fd3928f-90f0-4238-b2b3-592896d694fd%2Fokay.png?v=1636753692841)

# Making the installer

Simply open up Disk Management, and format your USB as FAT32:

**Right click the Start Button on your task bar and select Disk Management.
You should see all of your partitions and disks. On the bottom half, you'll see your devices. Find your USB.
You'll want to format the USB to have a FAT32 partition.
If you have multiple partitions on the USB, right click each partition and click Delete Volume for your USB (This will remove data, make sure you have backups and only remove partitions from your USB)
Right click the unallocated space and create a new simple volume. Make sure it is FAT32 and at least a gigabyte or two big. Name it "EFI".
Otherwise, right click the partition on the USB and click Format and set it to FAT32.

![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/DiskManagement.aac12f25.jpg)

Next, go to the root of this USB drive and create a folder called *com.apple.recovery.boot.* Then move the downloaded BaseSystem or RecoveryImage files. Please ensure you copy over both the .dmg and .chunklist files to this folder:
![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/com-recovery.805dc41f.png)

Now grab OpenCorePkg you downloaded earlier and open it:
![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/base-oc-folder.9a1a058a.png)

Here we see both IA32(32 Bit CPUs) and X64(64 Bit CPUs) folders, choose the one that's most appropriate to your hardware and open it. Next grab the EFI folder inside and place this on the root of the USB drive along side com.apple.recovery.boot. Once done it should look like this:

![alt text](https://dortania.github.io/OpenCore-Install-Guide/assets/img/com-efi-done.a6fb730e.png)

Now with all this done, head to [Setting up the EFI](https://github.com/TrustedFloppa/Aspire-E5-575G-Hackintosh/blob/main/SettingUpTheEFI.md) to finish up your work
