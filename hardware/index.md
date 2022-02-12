---
sidebar_position: 1
---

# Introduction

There are 2 working versions of boards. v0.2 and v0.3. v0.3 is improved version of v0.2.

Both are successfully working in houses of our users.
Navigate on submenu to version you're interested in.

![boneIO frontpanel](/img/frontpanel.jpg)

boneIO is a compact IO controller for home automation. Main features of this controller are

- Compact size (27x11x6)cm - 15 DIN modules
- DIN rail compatibility
- Low price
- Open HSP (See below)

## Specification

![boneIO without case](/img/boneIO_v0_2_full_without_case.jpg)

- 52 digital inputs
- 7 analog to digital converters
- I2C
- RS485
- OLED display
- user switch
- 24V PSU input
- ADC VDD output
- 12-48V external PSU for digital inputs

You can choose from many different output boards:

- Relay Board 24x16A
- Relay Board 32x5A
- Relay Board 24x10A
- Shutter Board 32x10A
- SSR Dimmer Board

Every output board use i2c interface to connect to BBB. Output board could be used inside the main controller or outside as a expansion module.

![Boards](/img/boards.jpg)

## Open HSP

`boneIO` is an Open HSP initiative where everything is open on [GPL-3.0 License](https://github.com/boneIO-eu/boneIO/blob/main/LICENSE)

- H (Hardware) stands for projects of electronic boards which you can print yourself
- S (Software) stands for ready to use firmware you can use on printed hardware
- P (Printables) stands for cases and other plastic elements you can print on a 3D printer and use with our hardware

With all elements in place, you can assemble a complete device. You can use it as-is or fork and modify it for your needs.

## Star topology

boneIO was designed to work with star topology. That's mean that you have specific cable to every electrical point for example every lamp and every switch should be connected directly to boneIO.

Here you can find some info how to plan this kind of electrical instalation:

<iframe src="https://www.youtube.com/embed/6winSE5_7IE" frameborder="0" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true" width="640" height="480"></iframe>