# Kabellos Pmod&trade; compatible module

Kabellos is a WiFi+Bluetooth Pmod&trade; compatible module based on the ESP32-C3-MINI-1 module.

![Kabellos](https://github.com/machdyne/kabellos/blob/c47c4434612ec16a9ce001880813e0f13db4362c/kabellos.png)

This repo contains schematics and pinouts. For a usage example, see the [Zucker SOC](https://github.com/machdyne/zucker).

Find more information on the [Kabellos product page](https://machdyne.com/product/kabellos-wireless-pmod/).

## Modes

The operating mode is selected by jumper J1:

 * Open: Pmod&trade; compatible wireless bridge powered by PMOD host
 * Short: Standalone wireless USB-powered device

### Warnings

 * Do not plug Kabellos into a PMOD socket when J1 is short.

## Firmware

Kabellos ships with the [ESP-AT](https://docs.espressif.com/projects/esp-at/en/latest/esp32c3/Get_Started/What_is_ESP-AT.html) firmware. The MicroUSB port can be used for debugging and updating the flash.

## Pinout

| Pin | Signal | ESP | Firmware |
| --- | ------ | --- | -------- |
| 1 | ESP\_EN | EN | EN (active high) |
| 2 | ESP\_BOOT | GPIO9 | BOOT (active low) |
| 3 | ESP\_TX | GPIO21 | TX (pmod to host) |
| 4 | ESP\_RX | GPIO20 | RX (host to pmod) |
| 5 | GND | - | |
| 6 | 3V3 | - | |
| 7 | ESP\_GPIO2  | GPIO2 | - |
| 8 | ESP\_GPIO6  | GPIO6 | - |
| 9 | ESP\_GPIO7 | GPIO7 | CTS |
| 10 | ESP\_GPIO10 | GPIO10 | RTS |
| 11 | GND | - | - |
| 12 | 3V3 | - | - |

Notes: ESP\_EN and ESP\_BOOT have pull-up resistors. Kabellos also has 3 testpoint pads that provide access to the ADC via GPIO5, GPIO4 and GPIO0.
