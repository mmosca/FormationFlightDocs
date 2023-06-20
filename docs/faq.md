# FAQ

## Who is FormationFlight for?

FormationFlight runs in tandem with your flight control software (Betaflight, iNav, or Ardupilot). It relays information about UAVs in the area to the flight controller for display on the OSD. FormationFlight uses LoRa or ESPNOW to broadcast position, altitude, speed and aircraft name, and listens for other UAVs so your flight controller's OSD can display this information

## What relation does this have to iNav Radar?

FormationFlight started as a fork of [iNav Radar by OlivierC](https://github.com/OlivierC-FR/ESP32-INAV-RADAR) to add a few hardware targets, but rapidly grew into a substantially different project. It was renamed and detached from iNav Radar in June of 2023. The old project's name (ESP32-INAV-RADAR) quickly became invalid once it ran on ESP8266 and with Ardupilot and Betaflight, so a new name was chosen: FormationFlight

## What changes were made as compared to iNav Radar?

*Many* features were added over the development process, but the highlights are:

* Increased update rate from 1Hz to 10Hz
* Support 6 simultaneous users rather than 4
* Add encryption support for privacy
* Port codebase to run on both ESP8266 & ESP32
* Added 2.4GHz LoRa support
* Added a WiFi configuration and monitoring system
* Added WiFi OTA firmware updates
* Added support for the ESP series built-in espnow functionality, which uses the internal WiFi chip.
* Support directly-attached GPS & MSP GPS injection so F411 boards can be used with FF
* Significantly rewrote and refactored the code into modules (Display, Config, etc.) for easier maintenance

## What do I need to use FormationFlight?

You'll need a small radio attached to your flight controller that communicates with other FormationFlight users. The preferred hardware choice are 2.4GHz receivers intended for the [ExpressLRS](https://github.com/ExpressLRS/ExpressLRS) project. These receivers are extremely small (10mm x 10mm), lightweight (0.5g), and inexpensive ($10 USD) compared to other hardware choices. They communicate over 2.4GHz LoRa and can achieve ranges of 3-5km easily, with some hardware capable of significantly more.

## I need help, where can I find more information?

Join our friendly Discord server! FormationFlight developers and users hang out in \#help-and-support 

[Join our Discord :fontawesome-brands-discord:](https://discord.gg/npaX3VxQjh){ .md-button }
