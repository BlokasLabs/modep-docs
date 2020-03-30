# Troubleshooting

## No Sound Or "Add Device Error" Happens Or UI Won't Open

First of all, check input and output cables, volume and gain level.
Also ensure that all the critical services are running, if one of them failed, the UI won't be accessible. Start fixing from the `jack` service errors,
then `modep-mod-host` and finally `modep-mod-ui`. Most likely cause of issues is Jack misconfiguration. Use `patchbox` utility to reconfigure it, or
edit `/etc/jackdrc` manually.

Try restarting the MODEP software:

1. Login via `ssh`.
1. Run:
    ```
    sudo systemctl stop modep-mod-ui modep-mod-host jack
    sudo systemctl start jack modep-mod-host modep-mod-ui
    ```
1. After the services are restarted, the browser should reload automatically.
1. Check status of the services:
    ```
    sudo systemctl status jack
    sudo systemctl status modep-mod-host
    sudo systemctl status modep-mod-ui
    ```
1. The status should be **'active (running)'**. If it's not, try checking the service logs for any errors:
    ```
    sudo journalctl -u jack
    sudo journalctl -u modep-mod-host
    sudo journalctl -u modep-mod-ui
    ```

If any of the service is not running, the UI won't open either. Most common problem is Jack misconfiguration. See (Setup)[Setup.md#configuring-the-sound-card] for information on how to reconfigure Jack.

## Distorted Sound
1. First check if Clip LED on your sound card (if any) is lit up while audio input signal is playing.
1. If it is:
    1. Turn down 'GAIN' knob until the Clip LED no longer gets turned on. If the 'GAIN' is at minimum, turn down the output volume of the device connected to your card’s Audio Input.
1. If you still get distorted sound after above is resolved. try experimenting with [Jack](Setup.md#configuring-the-sound-card), in particular the sampling rate, buffer size and period values.
Especially if XRUNs are being reported in the UI.
