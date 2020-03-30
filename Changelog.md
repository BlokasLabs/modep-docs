# Changelog

## 2020-03-14

* MODEP refactored to be a suite of [Debian packages](https://github.com/BlokasLabs/modep-debs)
* MODEP now runs as user `modep`, uses shared Jack backend.
* Built for `buster` Debian release.
* All plugins updated to whatever was the latest version available
* MOD software updated to version 1.8.

## 2018-08-31

### Overview of the changes:

* Pisound App can now be used to switch pedalboards
* `touchosc2midi` integrated by default - connect to MODEP WiFi hotspot and use 172.24.1.1 IP as the destination in TouchOSC compatible software.
* Realtime kernel
* OS and MOD DUO updated to latest version available

### Detailed changelog:

* Latest Raspbian Lite packages as of 2018.08.31
* mod-ui updated from 2017.03.28 to 2018.05.29 ([changelog](https://github.com/BlokasLabs/mod-ui/pull/3))
* mod-host updated from 2017.04.11 to 2017.09.05 ([changelog](https://github.com/BlokasLabs/mod-host/pull/1/commits/1726ad06b11323da7e1aaed690ff8aef91f702b5))
* `touchosc2midi` integrated and enabled by default
* Pisound hotspot name renamed to MODEP
* Realtime Linux kernel integrated, [v4.14.59-rt37](https://github.com/BlokasLabs/rpi-kernel-rt/releases/tag/v4.14.59-rt37)
* Added [MODEP scripts](https://github.com/BlokasLabs/modep-ctl-scripts) for Pisound App
* System log rotation made more frequent to avoid running out of disk space when running for long periods of time without rebooting
* Use performance CPU scaling governor by default

## 2018-04-03

* Support Raspberry Pi 3B+ out of the box.
* --period argument for Jack changed to -p 128 from -p 256.
* Based on latest Raspbian Stretch Lite OS

## 2018-01-22

* 294 plugins (was 144 before)
* mDNS enabled by default

## 2017-04-23

* Initial MODEP version released
