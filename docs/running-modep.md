# Running MODEP

![modep-default](https://raw.githubusercontent.com/wiki/BlokasLabs/modep/images/modep-default.png)

After having enabled the MODEP module in `patchbox` utility, you have to use a browser on your computer or tablet, or even the Raspberry Pi itself if you have a mouse and a monitor hooked up, to open the MODEP UI page.

If your device is connected to the Patchbox WiFi hotspot (default password is **`blokaslabs`**), try to open one of the URLs:

* http://172.24.1.1/
* http://patchbox.local/ [^1]
* http://127.0.0.1/ - Only if on Raspberry Pi itself.

[^1]: \*.local domain addresses depend on mDNS service. Up to date Linux and MAC OSes support it by default, while Windows 10 requires installing [Apple's Bonjour Print Services for Windows](https://support.apple.com/kb/DL999?locale=en_US)

///Footnotes Go Here///

Otherwise, your devices must be connected to the same local network, you should [find the IP](faq.md#determining-the-ip-address-of-your-pi) of the Raspberry Pi and use it with the http:// prefix. In case of any issues, take a look at [Troubleshooting](troubleshooting.md).

And that’s it! Now you can start building your pedalboards.

For more information on the MOD-UI follow this link (note that some usage and UI differences may be present): https://wiki.moddevices.com/wiki/MOD_Web_GUI_User_Guide

## LV2 Plugins Dir And Other Important Locations

The LV2 Plugins Dir for MODEP is located here: `/usr/modep/lv2/`. After making changes to the directory contents, reload MODEP:

```
sudo systemctl restart jack modep-mod-ui
```

The local pedalboards and settings are located here: `/var/modep/`

## TouchOSC clients

You may use [TouchOSC](https://hexler.net/software/touchosc) compatible clients on mobile devices to MIDI-map pedal controls. You must be connected to the same local network, and use the IP of Raspberry Pi for the TouchOSC Bridge IP (Host IP) in the app's settings.

## MOD Documentation

You can find extensive MOD Documentation on MOD Devices website: https://wiki.moddevices.com/wiki/Manual

Some of the features may be disabled or unavailable in MODEP due to differences in the hardware.
