# Running MODEP

![modep-default](https://raw.githubusercontent.com/wiki/BlokasLabs/modep/images/modep-default.png)

- Mount your freshly baked SD card to your Pi and power it up.
- Connect to it via “**MODEP”** Wi-Fi hotspot using your computer or tablet (**psw:blokaslabs**).
- Open your computer’s or tablet’s browser and go to this address [http://modep.local](http://modep.local)* or [http://172.24.1.1](http://172.24.1.1/) (you should see a similar view to the image above).
- That’s it. Now you can start building your pedalboards.

> \*.local domain addresses depend on mDNS service. Up to date Linux and MAC OSes support it by default, while Windows 10 requires installing [Apple's Bonjour Print Services for Windows](https://support.apple.com/kb/DL999?locale=en_US)

> **Note:** For more information on the MOD-UI follow this link (note that some usage and UI differences may be present): https://wiki.moddevices.com/wiki/MOD_Web_GUI_User_Guide

> **Note:** Jack service is running as 'root' user, in case you'd like to manually run jack_capture or other jack utils, it should be done as 'root' too.

## TouchOSC clients

You may use [TouchOSC](https://hexler.net/software/touchosc) compatible clients on mobile devices to MIDI-map pedal controls. You must be connected to the MODEP WiFi, and use `172.24.1.1` for the TouchOSC Bridge IP (Host IP) in the App's settings.

## MOD Documentation

You can find extensive MOD Documentation on MOD Devices website: https://wiki.moddevices.com/wiki/Manual

Some of the features may be disabled in MODEP due to differences in the hardware.
