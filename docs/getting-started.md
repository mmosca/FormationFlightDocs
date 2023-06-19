# Getting Started with FormationFlight

## Connect

For some boards (ESP dev boards like the Lolin or TTGO series) this can be done with a USB connection. For others like ExpressLRS receivers, you must use an external UART interface, commonly referred to as "an FTDI". 

### Connect boards with USB

Flashing dev boards with USB is easy! Just connect your board via USB and continue to the flashing section below

### Connect boards without USB

To flash boards without built-in USB, you'll need a UART interface. An example of one of these boards is [here](https://www.amazon.com/FT232RL-Adapter-Breakout-Converter-Arduino/dp/B08B878T7T).

Connect your board according to the diagram below.

![UART flashing diagram](/assets/images/FTDIConn.png)

Now you'll need to put the board into bootloader mode - this is done by connecting the GPIO0 pin to ground. On ExpressLRS receivers for example, there's a pad marked "BOOT". This pad must be connected to ground while power is applied to the board to enter bootloader mode. Once your board is in bootloader mode, continue to the flashing section.

## Flash

### Install ESP flasher

You can download an easy to use ESP flasher tool from [Jason8266's ESP\_Flasher repo](https://github.com/Jason2866/ESP_Flasher/releases). This tool makes it easy to install the FormationFlight firmware on your ESP board of choice.

### Download pre-built binaries

A simple way to install FormationFlight is by downloading pre-built binaries from [GitHub Releases](https://github.com/FormationFlight/FormationFlight/releases/latest). Choose the correct binary file for your board (for example, `expresslrs_rx_2400` for a 2.4GHz ExpressLRS receiver without PA/LNA like the HappyModel EP1/EP2).

### Flash your board

Configure ESP-Flasher with the serial port of your board, and select the firmware.bin file for your board

![ESP-Flasher screenshot](/assets/images/ESP-Flasher_pi0pgRDAuP.png)


## Configure

FormationFlight is designed to require minimal configuration of its own. Your flight controller software however will need to be configured to talk to FormationFlight

### iNav

iNav includes native support for FormationFlight. Follow their documentation on enabling the HUD [here](https://github.com/iNavFlight/inav/wiki/OSD-Hud-and-ESP32-radars#esp32-lora-modem-inav-radar-project) and **don't forget to enable the crosshair OSD element**.

### Ardupilot

As of 2023-06, Ardupilot does not yet natively support FormationFlight. However, the FormationFlight development team has an early release fork of Ardupilot which supports FormationFlight, available [here](https://github.com/MUSTARDTIGERFPV/Ardupilot). Be warned that this is prerelease software. Assume that it will crash your plane, kick your dog, and set your house on fire. With that in mind, the developers have been flying this modified version for a few months now without issue.

### Betaflight

As of 2023-06, Betaflight does not yet natively support FormationFlight. However, the FormationFlight development team has an early release fork of Betaflight which supports FormationFlight, available [here](https://github.com/MUSTARDTIGERFPV/Betaflight). Be warned that this is prerelease software. Assume that it will crash your quad, kick your dog, and set your house on fire. With that in mind, the developers have been flying this modified version for a few months now without issue.


## OTA Updates

FormationFlight includes an OTA (over-the-air) upgrade system, so future firmware upgrades can be done via WiFi.
