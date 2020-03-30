# Setup

Since version 2020-03-14 (1.8.0), MODEP is a module of [Patchbox OS](https://blokas.io/patchbox-os/).

## Patchbox OS

[Patchbox OS](https://blokas.io/patchbox-os/) comes with a config utility that helps with installing and managing the installed software and the system.

Once you have Patchbox OS running (refer to its [documentation](https://blokas.io/patchbox-os/docs/) for help), open the config utility by running:

```
patchbox
```

Navigate to the `modules` menu, and activate the `modep` module - it will install it and set it up to be run on startup.

To stop it from autostarting every time the system is turned on, select the `none` module in the `modules` menu of `patchbox` utility.

### Configuring The Sound Card

The first time Patchbox OS is started, a wizard runs that helps you configure your sound card. If you'd like to reconfigure it, simply run the below command, enter the 'jack' menu, then 'config' and follow the prompts.

```
patchbox
```

If you are using a sound card other than Pisound, you may have to tweak the volumes and card settings using `alsamixer`.

## Running It

Now continue with [Running MODEP](Running-MODEP.md). In case of any issues, take a look at [Troubleshooting](Troubleshooting.md).
