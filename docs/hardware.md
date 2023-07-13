# FormationFlight Hardware

## Supported Hardware

FormationFlight supports many targets for different hardware. If you don't see your hardware in this list, feel free to ask in the [FormationFlight Discord](https://discord.gg/npaX3VxQjh)

### ExpressLRS Hardware

Highly recommended for new users. The smallest, lightest, most affordable way to get started with FormationFlight.

| Target Name                           | Radios              | Supported Hardware                                                                          |
|---------------------------------------|---------------------|---------------------------------------------------------------------------------------------|
| `expresslrs_rx_2400`                  | 2.4GHz LoRa, ESPNOW | HappyModel EP1/EP2, RadioMaster RP1/RP2 BetaFPV Lite, Flywoo EL24E, Foxeer Lite, GEPRC Nano |
| `expresslrs_rx_2400_PA`               | 2.4GHz LoRa, ESPNOW | BetaFPV Nano, Jumper AION Nano, Matek R24-S                                                 |
| `expresslrs_rx_2400_AntennaDiversity` | 2.4GHz LoRa, ESPNOW | Matek R24-D, RadioMaster RP3                                                                |
| `expresslrs_rx_868`                   | 868MHz LoRa, ESPNOW | HappyModel ES900RX                                                                          |
| `expresslrs_rx_915`                   | 915MHz LoRa, ESPNOW | HappyModel ES900RX                                                                          |

### Legacy Targets

Legacy targets from iNav Radar are also supported in FormationFlight

| Target Name             | Radios              | Supported Hardware             |
|-------------------------|---------------------|--------------------------------|
| `diy_LoRa_lilygo10_433` | 433MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.0 433MHz |
| `diy_LoRa_lilygo10_868` | 868MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.0 868MHz |
| `diy_LoRa_lilygo10_915` | 915MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.0 915MHz |
| `diy_LoRa_lilygo14_433` | 433MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.4 433MHz |
| `diy_LoRa_lilygo14_868` | 868MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.4 868MHz |
| `diy_LoRa_lilygo14_915` | 915MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.4 915MHz |
| `diy_LoRa_lilygo16_433` | 433MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.6 433MHz |
| `diy_LoRa_lilygo16_868` | 868MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.6 868MHz |
| `diy_LoRa_lilygo16_915` | 915MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v1.6 915MHz |
| `diy_LoRa_lilygo20_433` | 433MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v2.0 433MHz |
| `diy_LoRa_lilygo20_868` | 868MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v2.0 868MHz |
| `diy_LoRa_lilygo20_915` | 915MHz LoRa, ESPNOW | TTGO/LILYGO LoRa32 v2.0 915MHz |

### DIY Targets

Targets for non-standard hardware that might be useful for a few folks. For example, the T-Beam has built-in OLED & GPS which is nice for a beacon not attached to an FC, such as inside a car or at a landing point

| Target Name                  | Radios              | Supported Hardware        |
|------------------------------|---------------------|---------------------------|
| `diy_LoRa_lilygo_t-beam_915` | 915MHz LoRa, ESPNOW | TTGO/LILYGO T-Beam 915MHz |


### ESPNOW Targets

ESPNOW is a fallback radio protocol for FormationFlight, supported on ESP chips without LoRa. Its max range is 1.5km under **ideal conditions** and more like 200m under normal conditions. Prefer LoRa in every case, but ESPNOW is left as an option for those who want to use it.

| Target Name                      | Radios | Supported Hardware                            |
|----------------------------------|--------|-----------------------------------------------|
| `diy_ESPNOW_esp8266`             | ESPNOW | Various ESP8266 dev boards / embedded devices |
| `diy_ESPNOW_wemosd1`             | ESPNOW | Wemos D1 Mini                                 |
| `diy_ESPNOW_lolin_d32`           | ESPNOW | LoLin D32 ESP32 dev board                     |
| `diy_ESPNOW_adafruit_qtpy_esp32` | ESPNOW | Adafruit QtPy ESP32 dev board                 |

