# Sound Card Setup

If you are using the Pisound sound card, you can skip this step. MODEP image comes with all the necessary Pisound software pre-installed so you can start playing around with the system straight away without making any modifications. 

If you are using a different sound card, connect to your Raspberry Pi via SSH following [this guide](faq#connecting-to-raspberry-pi-via-ssh) and complete the steps below in a terminal window to set your card as a default one:

1. Open a terminal window and enter `aplay -l`
2. Copy name of the sound card after ‘:' and before ‘[‘, for example `QUADCAPTURE`
3. Type `sudo nano /usr/lib/systemd/system/jack.service` and press Enter to edit the Jack service file
4. Replace `hw:pisound` with `hw:QUADCAPTURE` (Change `QUADCAPTURE` to the name of your sound card)
5. Hit Ctrl+X to close, press 'Y' to confirm saving your changes
6. Type `sudo reboot` and press Enter to restart the system

![](https://d2mxuefqeaa7sj.cloudfront.net/s_065861E88B4BC6E5846F284C5C9C3ACB680E7A1FD270C563898A163606732A5E_1534806168175_image.png)