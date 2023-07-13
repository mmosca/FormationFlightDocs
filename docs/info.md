# Info

## RF Bands & Frequencies

FormationFlight runs in multiple frequency bands using different radio systems. Given the nature of the system and its supported hardware, please be advised that use of the project is restricted to licensed amateur radio practitioners, and that it is your responsibility to conform with all applicable regulations for the environment where you'll be operating.

Frequency allocations and settings for the system can be seen in the following files:

* [Center frequencies per-band](https://github.com/FormationFlight/FormationFlight/blob/master/platformio.ini)
* [Modulation parameters sub-GHz](https://github.com/FormationFlight/FormationFlight/blob/master/src/lib/Radios/LoRa_SX127X.h)
* [Modulation parameters 2.4GHz](https://github.com/FormationFlight/FormationFlight/blob/master/src/lib/Radios/LoRa_SX128X.h)


Notably, the 2.4GHz frequency allocation & bandwidth used put FormationFlight below the 2.4GHz ISM band into the 13-centimeter amateur radio band. Operation in this band without a license is not permitted.

## Range

FormationFlight is offered on a range of hardware and radio systems. We strongly recommend 2.4GHz LoRa for the majority of users, as its ~10km range is more than sufficient for the majority of cases.

The estimates here consider the default transmit power (10dB for LoRa), and no occlusion. Your performance may vary.

| Radio Type  | Adjustments      | Estimated Sensitivity | Estimated Gain Adjustment | Estimated Ideal Range |
|-------------|------------------|-----------------------|---------------------------|-----------------------|
| ESPNOW      | PCB Antenna      | -80dBm                | -20dB                     | 200m                  |
| ESPNOW      | External Antenna | -80dBm                | -12dB                     | 500m                  |
| 2.4GHz LoRa | Ceramic Antenna  | -107dBm               | -5dB                      | 5km                   |
| 2.4GHz LoRa | Dipole Antenna   | -107dBm               | 0dB                       | 10km                  |
| 2.4GHz LoRa | LNA + Dipole     | -107dBm               | +10dB                     | 25km                  |
| 900MHz LoRa | Dipole Antenna   | -117dBm               | 0dB                       | 95km                  |
| 433MHz LoRa | Dipole Antenna   | -117dBm               | 0dB                       | 200km                 |


## ESPNOW

ESPNOW is a protocol built in to ESP8266 and ESP32 microcontrollers. It's a short-range simple protocol for ad-hoc messaging. FormationFlight supports using both LoRa and ESPNOW. However, as of version 4.0.x, simultaneous use of LoRa and ESPNOW is not supported. It can be enabled manually, but it causes the internal timing and synchronization system to go awry. In the future, each radio protocol should have its own synchronization system so that ESPNOW & LoRa can be used simultaneously, and users with different LoRa frequencies can still fly together.
