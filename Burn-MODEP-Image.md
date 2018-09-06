# Burn MODEP Image

> **Default Login Details:** user: modep, password: blokaslabs
> 
> **Default Wi-Fi Hotspot:** SSID: MODEP, password: blokaslabs


## Step 01: Install Etcher

**Windows**

Download Etcher from [https://etcher.io/](https://etcher.io/). Double-click the *.exe file in Windows and follow the Etcher setup wizard. Run Etcher in Administrator Mode: right-click on Etcher and choose ‘Run as administrator’.

**macOS**

Download Etcher from [https://etcher.io/](https://etcher.io/). Drag the Etcher app to your Applications folder on a Mac and double-click to open it.

**Linux**

Download the AppImage file from [https://etcher.io/](https://etcher.io/). App Images are self-contained runtimes that do not require manual installation or root. They will run on pretty much every distro out there. After the download is complete, double-click the image to run it.

## Step 02: Download MODEP image
Download a prebuilt MODEP OS image from [here](https://blokas.io/modep/latest). If the image comes in *.zip format, unzip the file after it has downloaded. Double-click the file on Mac or Linux (or use unzip in a terminal window). In Windows, right-click the file and choose Extract All.

## Step 03: Select the image
Launch Etcher. Click Select Image button. Use the file manager window to locate the image you unzipped in the previous step. Click Open. The image will appear under Select Image, and Connect a drive will highlight red.

## Step 04: Insert your SD card
Attach your SD card to the computer. Etcher will select it automatically, but to be safe check that the SD card is listed correctly. Now click Flash! to write the image file to the SD card.

## Step 05: Writing the image
Etcher will format the SD card, before writing and verifying the image; this is shown by a progress bar. When done, remove the SD card, insert it into your Raspberry Pi, and power it up.
