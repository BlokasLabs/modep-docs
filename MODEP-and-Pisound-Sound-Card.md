# MODEP and Pisound Sound Card
## The Pisound’s Button

Here is the list of functions you can achieve using Pisound’s button.

| **Interaction**              | **Action**                                                                                                                 |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Click betwen 1 and 8 times   | Load the pedalboard from the first bank on your list at index corresponding to the number of clicks (see the image below). |
| Hold between 1 and 3 seconds | Toggle Bluetooth discoverability on/off. On state automatically times out in 3 minutes.                                    |
| Hold between 3 and 5 seconds | Turn Wi-Fi hotspot mode on/off.                                                                                            |
| Hold between 5 and 7 seconds | Turn your Raspberry Pi off.                                                                                                |



![modep-banks](https://raw.githubusercontent.com/wiki/BlokasLabs/pisound-docs/images/modep-banks.PNG)

## Pisound Mobile App

You can use the Pisound App to switch the pedalboards. Get the App [here](https://blokas.io/pisound/docs/Pisound-App/#android). The `pisound-ctl` is pre-installed in the MODEP image.

First you have to [pair](https://blokas.io/pisound/docs/Pisound-App/#connecting-to-the-raspberry-pi) your mobile device and MODEP - hold down the Pisound Button between 1 and 2 seconds to toggle Bluetooth Discoverability. While the device is in discoverable mode, the MIDI IN/OUT LEDs will keep flashing, and after 180 seconds the discoverable mode will be automatically turned off.

Run the Pisound App, head into the Scan menu, and pair up with MODEP.

Afterwards, in the Collections screen you should see MODEP category, and it will have a list of pedalboards that are added in the very first Bank in MOD UI.

![pisound-app](https://raw.githubusercontent.com/wiki/BlokasLabs/modep/images/modep-pisound-app.png)