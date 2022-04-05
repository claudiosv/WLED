# Welcome to TechnoGecko WLED! ✨

A fast and feature-rich implementation of an ESP32 webserver to control WS2812B LEDs. This repo has two branches:
`main` which tracks upstream Aircookie's main branch (their dev branch)
`soundreactive-dev` which tracks upstream atuline's development branch

SoundReactive forked off from WLED quite a while ago, and does not really track upstream very closely. As a result, the featureset has diverged. However, there is a good reason to use the SoundReactive fork: it has pretty much every feature we care about from WLED, and most importantly it supports *matrices*. Standard WLED has no concept of a 2D effect, only 1D effects. For example, with 2D effects you can have flames rising from the bottom of the vest. 1D effects can't do that. However, TechnoGecko vests, while being a single strand in software, are arranged in hardware to look like a matrix. The original unisparks/tgvest software is written with 2D effects only. The second reason to use the SoundReactive fork, is that if you hook up a microphone to your vest, it can produce sound reactive effects *locally*, on device, *without* network. This is impressive considering how much processing power near-realtime audio processing requires.

With this in mind, I will try and keep my branch synced with upstream and release builds from both branches, so you can decide whether having the latest WLED features is more important than having matrix and local sound reactivity (which none of the vests do) support.

## ⚙️ Features
- WS2812FX library integrated for over 100 special effects  
- FastLED noise effects and 50 palettes  
- Modern UI with color, effect and segment controls  
- Segments to set different effects and colors to parts of the LEDs  
- Settings page - configuration over network  
- Access Point and station mode - automatic failsafe AP  
- Up to 10 LED outputs per instance
- Support for RGBW strips  
- Up to 250 user presets to save and load colors/effects easily, supports cycling through them.  
- Presets can be used to automatically execute API calls  
- Nightlight function (gradually dims down)  
- Full OTA software updatability (HTTP + ArduinoOTA), password protectable  
- Configurable Auto Brightness limit for safer operation  
- Filesystem-based config for easier backup of presets and settings 

### If using `soundreactive-dev` branch:
- Audio input from several sources including MAX4466, MAX9814, MAX9184, INMP401, INMP441 (for ESP32) and line-in.
- Volume reactive visual effects for ESP32 devices.
- Frequency reactive visual effects for ESP32 devices.
- UDP sound synchronization with transmit and receive for ESP32 (ESP8266 is supported upstream on `ESP8266` branch).
- 2D visual effects for ESP32 devices.
- Squelch and gain settings for ESP8266 and ESP32 devices for the volume reactive visual effects.
- 2D settings for ESP32 devices.
- Frequency reactive sliders for ESP32 devices.

## 💡 Supported light control interfaces
- WLED app for [Android](https://play.google.com/store/apps/details?id=com.aircoookie.WLED) and [iOS](https://apps.apple.com/us/app/wled/id1475695033)
- JSON and HTTP request APIs  
- UDP realtime  
- Sync color of multiple WLED devices (UDP notifier)  
- Simple timers/schedules (time from NTP, timezones/DST supported)  

## 📲 Quick start guide and documentation

See the [original WLED documentation on their official site](https://kno.wled.ge)!

## 🖼️ User interface
<img src="/images/macbook-pro-space-gray-on-the-wooden-table.jpg" width="50%"><img src="/images/walking-with-iphone-x.jpg" width="50%">

## 💾 Compatible hardware

See [how to make a TechnoGecko vest](https://wiki.technogecko.org/orange_vest)!

## ✌️ Other

Licensed under the MIT license  
Credits [here](https://kno.wled.ge/about/contributors/)!
