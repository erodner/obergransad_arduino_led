# IKEA OBERGRÄNSÄD Kit as Internet Clock

This project demonstrates how to use the IKEA OBERGRÄNSÄD kit as an internet clock using an ESP8266. The project includes improvements in WiFi connectivity and a reduction of refresh cycles.

The original code is from https://github.com/MakeMagazinDE/Obegraensad with the following changes:
* WiFi improvement for faster connection by https://github.com/softplus/esp8266-wifi-timing
* Dealing with WiFi meshes by selecting the BSSID with the best signal strength (this was critical in my case) - ER, 2024
* Changing the refresh cycles from one second to one minute - ER, 2024

## Introduction

This project utilizes the IKEA OBERGRÄNSÄD kit to create an internet-connected clock. The clock synchronizes time using an NTP server and displays it on a panel.

## Required Hardware Components

- ESP8266 with WiFi connectivity
- IKEA OBERGRÄNSÄD
- Required wiring cables

## Wiring and preparing the display

See the blog post in https://www.heise.de/select/make/2023/6.

## Setup

1. Clone the repository.
2. Install the required libraries (Arduino IDE):
    - `ESP8266WiFi`
3. Create a `secrets.h` file with your WiFi credentials:
    ```cpp
    #define WIFI_SSID "your-ssid"
    #define WIFI_PASSWORD "your-password"
    ```
4. Upload the code to your ESP8266.

## Further reading

1. The project at https://trandi.wordpress.com/2022/12/24/game-on-ikea-obergransad-led-display/ could be also fun to try out.