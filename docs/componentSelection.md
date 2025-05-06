---
title: Component Selection
---
## Component Selection

### Role

Before we discuss component selection, I will provide a brief description of my role in Team 202. My role in team 202 is head of the wifi module. My system will connect to wifi, and through an application or web service our user will be able to manipulate our exhibit. My system will communicate to another team member's system and they will communicate to another, resulting in a daisy chain of systems, through this daisy chain process my device will be able to communicate the users responses to other portions of the exhibit and deliver the response the user initiated.

### Components

#### Microcontroller Selection

| Solution | Pros | Cons|
|----------|------|-----|
|Option 1<br>![ESP32-S3-WROOM-1-N4](./microconSelect.png)<br>ESP32-S3-WROOM-1-N4<br>$2.95/Each<br>[RF TX/RX MOD BT WIFI PCB TH SMD](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)|<li>We use in class</li><li>Don't have to download new software to program</li>|<li>Many unused pins</li>|

##### Rationale Microcontroller

I decided on the ESP32-S3-WROOM-1-N4 to meet project requirements as well as I am familiar with the dev board. The ESP32 also comes with a built-in antenna allowing the team to connect to our exhibit wirelessly as well as meets two of the project requirements.

#### Switching Voltage Regulator

| Solution | Pros | Cons|
|----------|------|-----|
|Option 1<br>![LM2575D2T-3.3R4G](./option1SVR.png)<br>LM2575D2T-3.3R4G<br>$3.32/Each<br>[IC REG BUCK 3.3V 1A D2PAK-5](https://www.digikey.com/en/products/detail/onsemi/LM2575D2T-3-3R4G/1476688?s=N4IgTCBcDaIDIFkwFYDsyAiYAqBaAzAHT4BKALAOIgC6AvkA)|<li>We used one similar in class</li><li>Easy to solder</li>|<li>Frequency switching is much smaller than option 2</li>|
|Option 2<br>![LM2575-3.3WU-TR](./option2SVR.png)<br>LM2575-3.3WU-TR<br>$1.75/Each<br>[IC REG BUCK 3.3V 1A TO263-5](https://www.digikey.ch/en/products/detail/microchip-technology/LM2575-3-3WU-TR/1027646)|<li>Easy to solder</li>|<li>Less heat resistant than option 1</li>|
|Option 3<br>![TPS62162DSGR](./option3SVR.png)<br>TPS62162DSGR<br>$1.38/Each<br>[IC REG BUCK 3.3V 1A 8WSON](https://www.digikey.ch/en/products/detail/texas-instruments/TPS62162DSGR/2833447)|<li>Small, so saves space on a PCB.</li>|<li>Potentially difficult to solder</li>|

##### Rationale Voltage Regulator

My choice for the switching voltage regulator is option 1, LM2575D2T-3.3R4G. This component was chosen due to being familiar with the through hole version. It was also chosen due to the component being potentially the easiest to solder.

#### Summary Table

| Final Selection                               | Summary |
| --------------------------------------------- | ------ |
| ESP32-S3-WROOM-1-N4                           | The ESP32, is the brain of the board. Developed by Espressif Systems, it has a built in wifi and bluetooth module being ideal for IoT applications, wireless communication and embedded systems that require low-power connectivity.  |
| LM2575D2T-3.3R4G (Fixed voltage regulator)    | Designed by Onsemi, the buck switching regulator provides a stable 3.3V output while delivering 1A of current.|

## ESP32-S3-WROOM-1-N4 Diagram and Table

![ESP32 Pinout](./esp32Pinout.png)

| ESP Info                                      | Answer |
| --------------------------------------------- | ------ |
| Model                                         | ESP32-S3-WROOM-1-N4      |
| Product Page URL                              | [Product page](https://www.espressif.com/en/products/modules) |
| ESP32-S3-WROOM-1-N4 Datasheet URL             | [ESP32-S3-WROOM-1-N4](https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf)      |
| ESP32 S3 Datasheet URL                        | [ESP32-S3](https://espressif.com/documentation/esp32-s3_datasheet_en.pdf)      |
| ESP32 S3 Technical Reference Manual URL       | [Technical Manual](https://espressif.com/documentation/esp32-s3_datasheet_en.pdf)      |
| Vendor link                                   | [Digikey](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)      |
| Code Examples                                 | None can be found.      |
| External Resources URL(s)                     | Wifi beginners guide [video](https://www.youtube.com/watch?v=aH3sLEQI4_w)      |
| Unit cost                                     | $2.95      |
| Supply Voltage Range                          | 3V / 3.3V / 3.6V      |
| Absolute Maximum current <br> (for entire IC) | Not Stated/ MIN current: 500mA     |
| Maximum GPIO current <br> (per pin)           | 20mA, 1500mA total      |
| Supports External Interrupts?                 | Yes, only 1.     |
| Required Programming Hardware, Cost, URL      | MPLAB / FREE / [Link to MPLAB](https://www.microchip.com/en-us/tools-resources/develop/mplab-x-ide)      |

| Module         | # Available | Needed | Associated Pins (or * for any) |
| -------------- | ----------- | ------ | ------------------------------ |
| UART           | 2           | 2     | IO17(10), IO18(11)                              |
| External SPI   | 36           | 0      |                               |
| I2C            | 26           | 0      |                               |
| GPIO           | 36           | 2      | IO15(8), IO47(24)             |
| ADC            | 20           | 0      |                               |
| LED PWM        | 36           | 0      |                               |
| Motor PWM      | 36           | 0      |                               |
| USB Programmer | 2            | 2      | IO19(13), IO20(14)                              |

To create the MQTT subsystem, I had to choose components that can do such task. When choosing the major parts for my PCB, I start with researching components handled previously. Then I find similar components to create a table of components, listing out their pros and cons. Using the table I can choose the best component for the system. Results, were components handled previously due to getting the opportunity to get more familiar with them.

After major components were chosen, I then created the ESP32-S3-WROOM-1-N4 Diagram and Table. The template of the table was given by the instructor, but to populate it took research in the ESP32. I used my block diagram and many external resources, that I believe may help me append the ESP32 to my board and setup the device successfully, to complete the table. The results are a table I can reference when piecing my PCB together or troubleshooting it.

By choosing a voltage regulator that can handle switching voltage and a micro-controller with the ability to conduct wireless communication, I effectively meet product requirements.

## Power Budget

| Section | Component Name | Part Number | Supply Voltage Range | # | Absolute Maximum Current (mA) | Total Current (mA) | Unit |
|---------|----------------|-------------|----------------------|---|--------------------------------|--------------------|----|
| A. Major Components | ESP-32 | ESP32-S3-WROOM-1-N4 | 3.0V - 3.6V | 1 | NA | 1000 | mA |
| | +3.3V Regulator | LM2575D2T-3.3R4G | 3.234V - 3.366V | 1 | 3000 | NA | mA |
| B. +3.3V Power Rail | ESP-32 | ESP32-S3-WROOM-1-N4 | 3.0V - 3.6V | 1 | NA | 1000 | mA |
| | Subtotal | | | | | 1000 | mA |
| | Safety Margin | | | | | 25% | |
| | Total Current Required on +3.3V Rail | | | | | 1250 | mA |
| C. Regulator Choice | +3.3V Regulator | LM2575D2T-3.3R4G | 3.234V - 3.366V | 1 | 3000 | 1500 | mA |
| | Total Remaining Current Available on 3.3V Rail | | | | | 250 | mA |
| D. External Power Source 1 | Plug-in Wall Supply | Model:0930 | 100 - 240VAC | 9V | 3000 | 1500 | mA |
| Power Rails Connected to External Power Source 1 | ESP-32 | ESP32-S3-WROOM-1-N4 | 3.0V - 3.6V | 1 | 1000 | 1000 | mA |
| | +3.3V Regulator | LM2575D2T-3.3R4G | 3.234V - 3.366V | 1 | | 0 | mA |
| | Total Remaining Current Available on External Power Source 1 | | | | | 500 | mA |
| External Power Source 2 | USB | USB3131 | 30V | 3.3V | 1800 | 1500 | mA |
| Power Rails Connected to External Power Source 2 | ESP-32 | ESP32-S3-WROOM-1-N4 | 3.0V - 3.6V | 1 | 1000 | 1000 | mA |
| | +3.3V Regulator | LM2575D2T-3.3R4G | 3.234V - 3.366V | 1 | 3000 | | mA |
| | Total Remaining Current Available on External Power Source 2 | | | | | 500 | mA |
| External Power Source 3 | Team Power | NA | +9V | 3.3V | 3000 | 1500 | mA |
| Power Rails Connected to External Power Source 3 | ESP-32 | ESP32-S3-WROOM-1-N4 | 3.0V - 3.6V | 1 | 1000 | 1000 | mA |
| | +3.3V Regulator | LM2575D2T-3.3R4G | 3.234V - 3.366V | 1 | 3000 | | mA |
| | Total Remaining Current Available on External Power Source 3 | | | | | 500 | mA |

The power budget allows the team to coordinate their micro-controllers with each other. By gathering the information above, team 202 can decide whose board will initiate team power, as well as derive how much power the exhibit will consume. By calculating our consumption we can determine how much power we shall need as a team and how long our exhibit can operate.

In conclusion, the power budget is essential. If one is a part of a team, the team can append the system easier knowing the power consumption of the device being added. Lastly, the budget gives me a quick reference of my power needs and constraints. By estimating my system's maximum power I can choose the most appropriate and capable components to support my system.
