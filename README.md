# Hello Lora
## Simple Arduino-UNO/Dragino Lora Shield -Sketch to access [TTN](https://thethingsnetwork.org)

Heavily inspired by the work of [Andreas Spiess](https://www.youtube.com/watch?v=duwUwXt-hs8)

This Sketch will fire a message (*"Hello Lora"*) every 60 seconds the TTN-Network via the Dragino Lora Shield.

### Hardware
- Arduino UNO (or similar)
- [Dragino LoRa Shield](http://www.dragino.com/products/module/item/102-lora-shield.html)

### Setup

- Setup a new device in your TTN-Console. Be sure to set/change the activation method to `ABP` (Activation By Personalisation).
- Add [matthijskooijman/arduino-lmic](https://github.com/matthijskooijman/arduino-lmic)-library into [Arduino-IDE](https://www.arduino.cc/en/main/software). I downloaded from github an installed manually (*Sketch* > *Include Library* > *Add ZIP Library*).
- Copy `credentials.example.h` to `credentials.h` (ignored by git) and change (`NWKSKEY`, `APPSKEY`, `DEVADDR`) according to your TTN-Application-Device Keys in TTN.
- Compile and Run in Arduino-IDE.

### Notice
- **Be sure to know about TTN [Fair Access Policy](https://www.thethingsnetwork.org/forum/t/limitations-data-rate-packet-size-30-seconds-uplink-and-10-messages-downlink-per-day-fair-access-policy/1300) before running or changing the settings.**\
  [Here is a short explanation](https://www.youtube.com/watch?v=duwUwXt-hs8&t=11m1s).
- Change spreading factor in function `LMIC_setDrTxpow` (`DR_SF7`…`DR_SF12`).
- Change time between messages in const `TX_INTERVAL`.




