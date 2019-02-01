# Guides & FAQs

## Connecting to Raspberry Pi via SSH

- Connect to Raspberry Pi via "**MODEP**" Wi-Fi hotspot using your computer or smartphone/tablet (**psw:blokaslabs**) or connect your Raspberry Pi to your local network using an Ethernet cable.
- If connected via "**MODEP**" Wifi, the IP address is 172.24.1.1, otherwise find out the IP address of your Raspberry Pi following [this guide](faq#determining-the-ip-address-of-your-pi).
- Choose one of the following options based on the device you want to control your Pi with

> **Note:** the default username is 'modep' and the default password is 'blokaslabs'

**Option 01: Using Linux or macOS computer**

1. Connect your computer to the same Network as Raspberry Pi
1. Open a terminal window and type `ssh modep@IP_ADDRESS` (for the IP_ADDRESS use the IP address from the previous step)

**Option 02: Using Windows computer**

1. Download and install PuTTY software from https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
1. Connect your computer to the same Network as Raspberry Pi
1. Launch PuTTY client
1. Enter the IP address from the previous step and click Open

**Option 03: Using Android or iOS device**

1. Download Termius App from http://www.termius.com/
1. Connect your device to the same Network as Raspberry Pi
1. Open the Termius App
1. Enter an alias of your choosing
1. Enter the IP address from the previous step under hostname
1. Complete the username and password fields and hit Save in the top right corner

## Determining the IP Address of your Pi

**Step 00: MODEP Hotspot**

If you are connected to the Raspberry Pi via “**MODEP**” Wi-Fi hotspot, the Raspberry Pi’s IP is **172.24.1.1.** If that’s the case, you can skip the following steps. 😉

**Step 01: Connect your Raspberry Pi to your local Network**

Connect your Raspberry Pi to your local network using an Ethernet cable or Wi-Fi.

**Step 02: Find out the IP address**

**Option 01: Using monitor and keyboard**

1. Connect monitor and keyboard to your Raspberry Pi
2. Make sure your Raspberry Pi is powered on and wait for it to boot
3. Open a terminal window and type `ifconfig -a`
4. In the output you will see the `inet addr` line displaying the IP, e.g. 192.168.1.10

**Option 02: Using your tablet/smartphone & Fing App**

1. Download the Fing app via [https://play.google.com/store/apps/details?id=com.overlook.android.fing1](https://play.google.com/store/apps/details?id=com.overlook.android.fing) or [https://itunes.apple.com/gb/app/fing-network-scanner/id430921107?mt=8](https://itunes.apple.com/gb/app/fing-network-scanner/id430921107?mt=8)
2. Connect your tablet/smartphone to the same Network as Raspberry Pi
3. Open the Fing app and touch the refresh button in the upper right-hand corner of the screen
4. Scroll down to the entry with the manufacturer “Raspberry Pi”
5. You will see the IP address in the bottom left-hand corner

**Option 03: Using your computer & Ping command**

1. Connect your computer to the same Network as Raspberry Pi
2. Open a terminal window (Command Prompt on Windows)
3. Run the following command `ping modep.local`
  - On Windows PC, mDNS driver is required for .local addresses to work, you may install this service: [https://support.apple.com/kb/DL999?locale=en_US1](https://support.apple.com/kb/DL999?locale=en_US)
4. If the Raspberry Pi is reachable, ping will show its IP address, e.g:
    PING modep.local (192.168.1.33): 56 data bytes
    64 bytes from 192.168.1.33: icmp_seq=0 ttl=255 time=2.618 ms

**Option 04: Using your computer & Angry IP Scanner software**

1. Download and install Angry IP Scanner software via [http://angryip.org/](http://angryip.org/)
2. Connect your computer to the same Network as Raspberry Pi
3. Launch Angry IP Scanner and press Start button
4. Scroll down to the entry with your Raspberry Pi’s hostname
5. You will see the IP address in the column on the left

**Option 05: Router Web GUI**

1. Login into your local router via its webgui (usually something like [http://192.168.1.254](http://192.168.1.254/))
2. Go to network map or network overview.
3. Look up a device called raspberrypi or modep.
4. The IP should be listed somewhere there.


> **Note:** Your Raspberry Pi may have a different IP address depending on whether it’s connected to WiFi or Ethernet, and that address might even change from time to time. If you ever find yourself unable to connect, you can always double-check!


## Test Connectivity Between Pi and PC/Laptop
1. In a terminal window (`cmd` on Windows), run `ping <IP-Address>`
2. If connectivity is good, you should see response times getting logged.
  1. On Windows, by default 4 ping requests are made and the utility exits.
  2. On other OSes, by default you have to manually quit by hitting Ctrl+C.
  

## Editing MODEP Configuration Files

Here's a quick guide on how to modify system configuration files, such as `jack.service`. Once connected via `ssh`, use a text editor to edit the file, the most popular ones are covered here:


**nano**: A simple text editor with familiar user interface to GUI based notepads.


  1. `sudo nano /usr/lib/systemd/system/jack.service`
  1. Make your changes using cursor keys to navigate.
  1. Hit 'Ctrl+X' to close, press 'Y' to confirm saving your changes.


**vi**: A modal commands based text editor with rich features.

  1. `sudo vi /usr/lib/systemd/system/jack.service`
  1. Navigate to the place you want to change using h, j, k, l keys.
  1. Enter 'insert mode' by pressing 'i' key.
  1. Make your changes.
  1. Hit 'Esc' key to go back to command mode.
  1. Type :wq to write the changes and quit the editor.