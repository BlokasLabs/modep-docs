# Contribution Guide

## 'modep' Build Instructions

TBA


## Adding Additional Plugins

New plugins can be added to MODEP builds by adding a step in [Stage 5](https://github.com/BlokasLabs/modep/tree/modep/stage5) of the build, you will find there quite a variety of scripts for already integrated plugins on which you can base new additions. The rough steps of building a plugin are:

1. Checking out the source code
1. Build the plugin
1. Copy / install the resulting build into ${LV2_DIR} (/usr/local/modep/.lv2/)
1. Remove the temporary build files and the source code

Some useful information for building and developing plugins:

* https://github.com/moddevices/mod-plugin-builder - Build files for many plugins supported by MOD DUO
* https://github.com/moddevices/mod-lv2-data - modgui UIs for a lot of LV2 plugins
* https://github.com/moddevices/mod-sdk - modgui development tools
* http://moddevices.com/ns/modgui/ - modgui lv2 extension specification
