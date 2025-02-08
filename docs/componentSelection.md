---
title: Component Selection
---
# Component Selection

## Microcontroller Selection

| Solution | Pros | Cons|
|----------|------|-----|
|Option 1<br>![ESP32-S3-WROOM-1-N4](./microconSelect.png)<br>ESP32-S3-WROOM-1-N4<br>$2.95/Each<br>[RF TX/RX MOD BT WIFI PCB TH SMD](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)|<li>We use in class</li><li>Don't have to download new software to program</li>|<li>Many unused pins</li>|

## Switching Voltage Regulator

| Solution | Pros | Cons|
|----------|------|-----|
|Option 1<br>![LM2575D2T-3.3R4G](./option1SVR.png)<br>LM2575D2T-3.3R4G<br>$3.32/Each<br>[IC REG BUCK 3.3V 1A D2PAK-5](https://www.digikey.com/en/products/detail/onsemi/LM2575D2T-3-3R4G/1476688?s=N4IgTCBcDaIDIFkwFYDsyAiYAqBaAzAHT4BKALAOIgC6AvkA)|<li>We use one similar in class</li><li>Easy to solder</li>|cons|
|Option 2<br>![LM2575-3.3WU-TR](./option2SVR.png)<br>$1.75/Each<br>[IC REG BUCK 3.3V 1A TO263-5](https://www.digikey.ch/en/products/detail/microchip-technology/LM2575-3-3WU-TR/1027646)|pros|cons|
|Option 3<br>![TPS62162DSGR](./option3SVR.png)<br>$1.38/Each<br>[IC REG BUCK 3.3V 1A 8WSON](https://www.digikey.ch/en/products/detail/texas-instruments/TPS62162DSGR/2833447)|pros|<li>Potentially difficult to solder</li>|

### Rational


# ESP32-S3-WROOM-1-N4

| ESP Info                                      | Answer | Help                                                                                                      |
| --------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------- |
| Model                                         | ?      | Include the entire part number (leave off any letters at the end that specify the package type)           |
| Product Page URL                              | ?      | [Product page](https://www.espressif.com/en/products/modules) found here. com                                                                                    |
| ESP32-S3-WROOM-1-N4 Datasheet URL             | ?      | Do not paste links directly into the table.  Use a [ESP32-S3-WROOM-1-N4](https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf)                                              |
| ESP32 S3 Datasheet URL                        | ?      | [ESP32-S3](https://espressif.com/documentation/esp32-s3_datasheet_en.pdf) functions                                                                              |
| ESP32 S3 Technical Reference Manual URL       | ?      | [Technical Manual](https://espressif.com/documentation/esp32-s3_datasheet_en.pdf)                                                          |
| Vendor link                                   | ?      | [Digikey](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)                       |
| Code Examples                                 | ?      | url(s) for libraries on github or other sites related to the microcontroller and your planned peripherals |
| External Resources URL(s)                     | ?      | Search on Google and YouTube for other resources for each specific microcontroller.                       |
| Unit cost                                     | ?      | $2.95                                                                |
| Absolute Maximum Current for entire IC        | ?      | 500mA                                                                     |
| Supply Voltage Range                          | ?      | Min / Nominal / Max / Absolute Max, as found in datasheet                                                 |
| Absolute Maximum current <br> (for entire IC) | ?      | as found in datasheet                                                                                     |
| Maximum GPIO current <br> (per pin)           | ?      | as found in datasheet                                                                                     |
| Supports External Interrupts?                 | ?      | as found in datasheet                                                                                     |
| Required Programming Hardware, Cost, URL      | ?      | as found in datasheet                                                                                     |

| Module         | # Available | Needed | Associated Pins (or * for any) |
| -------------- | ----------- | ------ | ------------------------------ |
| UART           | ?           | ?      | ?                              |
| external SPI\* | ?           | ?      | ?                              |
| I2C            | ?           | ?      | ?                              |
| GPIO           | ?           | ?      | ?                              |
| ADC            | ?           | ?      | ?                              |
| LED PWM        | ?           | ?      | ?                              |
| Motor PWM      | ?           | ?      | ?                              |
| USB Programmer | ?           | 1      | ?                              |
| ...            |
