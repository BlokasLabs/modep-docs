# Troubleshooting

## No Sound Or "Add Device Error" happens

First of all, check input and output cables, volume and gain level.
If this fails, then try restarting the MODEP software:

1. Login via `ssh`.
1. Run:
    ```
    sudo systemctl stop mod-ui mod-host jack
    sudo systemctl start jack mod-host mod-ui
    ```
1. After the services are restarted, the browser should reload automatically.
1. Check status of the services:
    ```
    sudo systemctl status jack
    sudo systemctl status mod-host
    sudo systemctl status mod-ui
    ```
1. The status should be **'active (running)'**. If it's not, try checking the service logs for any errors:
    ```
    sudo journalctl -u jack
    sudo journalctl -u mod-host
    sudo journalctl -u mod-ui
    ```

## Distorted Sound
1. First check if Clip LED on your sound card (if any) is lit up while audio input signal is playing.
1. If it is:
    1. Turn down 'GAIN' knob until the Clip LED no longer gets turned on. If the 'GAIN' is at minimum, turn down the output volume of the device connected to your card’s Audio Input.
1. If you still get distorted sound after above is resolved:
    1. Check XRUNS-Status at the lower right corner of your browser window.
1. Try experimenting with [jack](advanced/#advanced-audio-configuration) settings defined in `/usr/lib/systemd/system/jack.service`, in particular the -n, -p, -r values. See [here](faq.md#editing-modep-configuration-files) for instructions on how to edit it.