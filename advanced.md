# Advanced Audio Configuration

There's many different layouts of effects possible with very different processing requirements from one to another, so trade-offs between stability and latency have to be made when defining the default audio settings. 

If you'd like to try and achieve a lower latency or more stability (less XRUNs) for your use case, you may try one of alternative configurations out, see [here](faq#editing-modep-configuration-files) for editing instructions.

In a nutshell, the lower the audio buffer (based on -n and -p arguments), the lower is the latency, but also the lower is the stability. Same goes with the higher is the sampling rate (-r, check which values are supported by your sound card, e.g. Pisound supported values are 48000, 96000, 192000). So you have to balance these values to best accommodate your use case.

For more details on the arguments, see Jack's [documentation](https://github.com/jackaudio/jackaudio.github.com/wiki/jackd(1)).

The line to edit in `/usr/lib/systemd/system/jack.service` is [this one](https://github.com/BlokasLabs/modep-gen/blob/modep/stage3/03-install-mod/files/jack.service#L9):

    ExecStart=/usr/bin/jackd -v -t 2000 -P 75 -d alsa -d hw:card_name -r 48000 -p 128 -n 2 -X seq -s -S

Try replacing with one of the below:

    ExecStart=/usr/bin/jackd -v -t 2000 -s -d alsa -d hw:card_name -r 96000 -p 256 -n 3 -X seq

If you happen to find a good command line to use, let us know via e-mail, support chat or in our community!

Once the config is changed, you must either restart the system:

    sudo reboot

or at least the MODEP's services:

    sudo systemctl stop mod-ui mod-host jack
    sudo systemctl daemon-reload
    sudo systemctl start jack mod-host mod-ui