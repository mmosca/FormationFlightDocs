# Setting up ArduPilot with FormationFlight

This document assumes you already have experience with Ardupilot, including manipulating parameters directly. If you're not familiar with this process, read through the [ArduPilot Documentation](https://ardupilot.org/plane/docs/introduction.html).

## Build

Presently, ArduPilot does not support FormationFlight natively. However, the FormationFlight development team has written a fork of ArduPilot.

In order to build ArduPilot with FormationFlight support, follow the [ArduPilot document on "building the code"](https://ardupilot.org/dev/docs/building-the-code.html), but clone [MUSTARDTIGERFPV's ardupilot fork repo](https://github.com/MUSTARDTIGERFPV/ardupilot) instead of the upstream. The rest of the build process is the same.

## Configure

You will need to adjust a few parameters directly; this can be done in Mission Planner through the [Full Parameter List](https://ardupilot.org/planner/docs/mission-planner-configuration-and-tuning.html#full-parameter-list).

### Enable Radar support

Set the Ardupilot parameter `RADAR_TYPE`. This must be set to `1` for MSP Radar, which is the only form supported at the moment.

### Set the serial port for MSP

Find the correct `SERIALX_PROTOCOL` instance for the serial port on which your Radar module is connected. You'll then set `SERIALX_PROTOCOL` to `32` for MSP


### Enable the Radar OSD

In the Onboard OSD section of Mission Planner, enable the `RADAR` element and set its X/Y positions. The current (2023-07) design takes up two lines of OSD space, the top for horizontal offset and the bottom for vertical. This may change in the future, but plan for 2 lines of space when placing it in your OSD.

The Radar OSD can be seen in the bottom-left of this screenshot (beginning with "C")

![ArduPilot Radar Screenshot](/assets/images/image-12.png)
