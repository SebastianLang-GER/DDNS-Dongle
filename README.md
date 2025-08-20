# ESP32 DDNS-Dongle
Firmware for an ESP32 based dynamic DNS (also DynDNS or DDNS) client to update a name server with the current WAN IP address.  
A web app hosted on the device itself allows easy configuration.

## Main Features
- WAN IP determination via [ipify API](https://www.ipify.org/)
- Update any DDNS service
- IPv4 and IPv6 support
- Easy configuration via web app
- Low power consumption (MCU deep sleep with programmable wake up)

## Requirements
### Hardware
Any ESP32 based hardware can be used. 
However, originally this firmware was designed for *ESP32 KEY v1.0* boards in the form factor of a USB dongle integrating an *Espressif Systems ESP32-PICO-D4* MCU and *WCH CH343P* USB-to-serial transceiver.  
![image of ESP32 KEY v1.0 USB dongle](/Media/ESP32%20KEY%20v1.0.png)

### Software
This firmware is written in C++ on the [Arduino platform](https://www.arduino.cc/), including the web app written in HTML, CSS and JavaScript.  
Pre-built binaries for direct flashing on *ESP32 KEY v1.0* are available on the [project release page](https://github.com/SebastianLang-GER/DDNS-Dongle/releases).  
For other hardware configurations you need to download this source code and compile it with [Arduino IDE 2](https://docs.arduino.cc/software/ide/).

#### Dependencies
- [CH343 VCP driver](https://www.wch-ic.com/downloads/CH343SER_EXE.html) v1.9
- [Arduino core for the ESP32](https://github.com/espressif/arduino-esp32) v3.3.0
- [AsyncTCP](https://github.com/ESP32Async/AsyncTCP) v3.4.7
- [ESPAsyncWebServer](https://github.com/ESP32Async/ESPAsyncWebServer) v3.8.0
- [ArduinoJson](https://github.com/bblanchon/ArduinoJson) v7.4.2

#### Compiler Configuration
- Board: ESP32 PICO-D4
- Partition scheme: Default
