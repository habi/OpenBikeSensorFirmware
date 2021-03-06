# OpenBikeSensor

Distance Measurement HC-SR04 ultrasonic sensors connected to ESP32

## Description

Inspired by the Berlin project Radmesser. This version uses a simple bush button to confirm distances measures were actually overtaking vehicles. It has its own GPS and SD card for logging, so it does not require additional hardware like a smartphone.

## Getting Started

### Hardware

The prototype by [Zweirat](https://zweirat-stuttgart.de/projekte/openbikesensor/) used the following:
* [ESP32](https://www.az-delivery.de/products/esp32-developmentboard)
* [HC-SR04P](https://www.ebay.de/itm/183610614563)
* [5-pin XS9 Aviation Connector](https://www.aliexpress.com/item/32512693653.html)
* [12mm Push Button](https://www.aliexpress.com/item/4000295670163.html)
* [0.96 inch OLED Display](https://www.aliexpress.com/item/32896971385.html)
* [USB-C Charging Module](https://www.ebay.de/itm/173893903484)
* [GPS Module](https://www.ebay.de/itm/GPS-NEO-6M-7M-8M-GY-GPS6MV2-Module-Aircraft-Flight-Controller-For-Arduino/272373338855)
* Plenty of wires (0.25mm^2) and heat-shrink tubing

To power the sensor you have a choice of Lithium-Iron or Lithium-Ion batteries
* [Automatic Buck-Boost Step Up Down Module for LiPo usage](https://www.ebay.de/itm/264075497616)
* [LiIon battery](https://www.akkuparts24.de/Samsung-INR18650-25R-36V-2500mAh-Li-Ion-Zelle)
or
* [Battery-Protection-Board](https://www.ebay.de/itm/202033076322)
* [LiFePo charging module](https://www.ebay.de/itm/MicroUSB-TP5000-3-6v-1A-Charger-Module-3-2v-LiFePO4-Lithium-Battery-Charging-/122164745507)
* [LiFePo-Battery](https://www.akkuteile.de/lifepo-akkus/18650/a123-apr18650m-a1-1100mah-3-2v-3-3v-lifepo4-akku/a-1006861/)

Li-Ion batteries are usually cheaper and have higher capacity at the same size. Lithiom-Iron batteries are considered quite safe.

Screws and nuts:
* [1x M5x35](https://www.amazon.de/gp/product/B078TNC9H1)
* [2x M4x30](https://www.amazon.de/gp/product/B01IMGZTT0)
* [7x M3x45](https://www.amazon.de/gp/product/B07KTBYPFP)
* [4x M2x12](https://www.amazon.de/gp/product/B078TQYZVX)
* [1x M2x10](https://www.amazon.de/gp/product/B01GQX070W)

* [1x M5 Mutter](https://www.amazon.de/gp/product/B07961ZH1B)
* [2x M4 Mutter](https://www.amazon.de/gp/product/B07961ZH19)
* [7x M3 Mutter](https://www.amazon.de/gp/product/B01H8XN99A)
* [5x M2 Mutter](https://www.amazon.de/gp/product/B01H8XN7VK)

You can consider getting slotted-head screws for the M2 ones if you are worried about damaging the tiny Allen screws.

### Dependencies

* ESP32 device driver
* Arduino IDE
* [TM1637 Library](https://github.com/avishorp/TM1637) - installed through Arduino library manager
* [SSD1306 Library](https://github.com/adafruit/Adafruit_SSD1306) - installed through Arduino library manager
* [TinyGPSPlus Library](https://github.com/mikalhart/TinyGPSPlus)

### Installing

* clone or download repository
* open in Arduino IDE
* compile and upload to ESP32
* Connect sensor

### Use
* power up device
* push the button each time there is a value shown in the display and you want to confirm it was a vehicle overtaking you
* power down

### Configuration
Most of the configuration is a stub and needs further development. But uploading new firmware works. You can enter the configuration mode by pushing the button while turning the device on. Then it will open a unique WiFi including the devices Macadress named "OpenBikeSensor-xxxxxxxxxxxx". Initial password is "12345678". The configuration page can be found on "http://openbikesensor.local" or "172.20.0.1". You can directly upload a precompiled binary.

## Acknowledgments

Inspiration, code snippets, etc.
* [Use of ArduinoJson Library](https://arduinojson.org/v6/example/config/)
* [Interface for OTA Web Updates by LastMinuteEngineers.com](https://lastminuteengineers.com/esp32-ota-web-updater-arduino-ide/)
