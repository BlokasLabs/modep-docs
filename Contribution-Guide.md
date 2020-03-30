# Contribution Guide

## Debian Packages

The MODEP consists of a lot of Debian packages, the scripts to build all of them are located here: https://github.com/BlokasLabs/modep-debs

To build them locally, first checkout the repository and all of its submodules:

```
git clone https://github.com/BlokasLabs/modep-debs.git --recursive
```

Then sort out the build dependencies:

```
cd modep-debs
./install-apt-build-dependencies.sh
```

Then you may run `./build-all.sh` to build all of the debs. It will take a while.

Instead you may execute `./build-deb.sh` in subfolder of interest to get only the particular deb package.

**Note:** The contents are always copied from `src` on top of `[package]-[version]` folder when executing `build-deb.sh`, so apply your changes in the `src` folder.

Please feel free to submit pull requests on `modep-debs` repository or submodule repositories, we'll take care of getting your changes into our APT server.

## Useful Resources

Some useful information for building and developing plugins:

* https://github.com/moddevices/mod-plugin-builder - Build files for many plugins supported by MOD DUO
* https://github.com/moddevices/mod-lv2-data - modgui UIs for a lot of LV2 plugins
* https://github.com/moddevices/mod-sdk - modgui development tools
* http://moddevices.com/ns/modgui/ - modgui lv2 extension specification
