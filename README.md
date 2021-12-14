# Aspire-E5-575G-Hackintosh
Supported Versions of Mac OS X
# Monterey (12.1) # Big Sur (10.16)  Catalina (10.15)  Mojave (10.14)  High Sierra (10.13)  Sierra (10.12)  El Capitan (10.11)

# Note
You will require lan cable to use online installer if you dont have lan cable then use Method 2 (Offline Installer)


# Method 1 : Online Installer

Make sure you downloaded efi from this repo and placed it into your usb

Download OpenCore From Here
https://github.com/acidanthera/OpenCorePkg/releases/download/0.7.6/OpenCore-0.7.6-RELEASE.zip


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

# Copy files you got in macrecovery to your usb and create new folder named com.apple.recovery

# Note: you cant use older installers like Yosemite, Mavericks , Mountain lion , and lion. Because of skylake processors arent supporting older than El capitan





# Offline Installer
### Thanks olarila for offline installer 😄
-Download Etcher-

https://github.com/balena-io/etcher/releases/download/v1.7.1/balenaEtcher-Setup-1.7.1.exe?d_id=b2a0dd08-4220-4144-92be-60a3bc5f3b1eR

--MONTEREY--

MediaFire Link - https://tinyurl.com/2p8fxsyk

--BIG SUR--

MediaFire Link - https://tinyurl.com/2ztn9nab

--CATALINA--

MediaFire Link - https://tinyurl.com/y3mlf4of   

--MOJAVE--

MediaFire Link - https://tinyurl.com/y4ls8a4t

--HIGH SIERRA--

MediaFire Link - https://tinyurl.com/ycq8d3ld

--SIERRA--

MediaFire Link - https://tinyurl.com/y6gqb2ya

--EL CAPITAN--

MediaFire Link - https://tinyurl.com/y37jwjpv
