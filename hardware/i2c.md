---
sidebar_position: 4
title: I2C Output Board Config
---

# I2C Configuration for Output Boards

## How to find config pins?

On every output board you will find some pins to configure I2C addresses of two MCP23017 expanders and one temperature sensor. In v0.2 it was placed on the top layer of the board, but from v0.3 you will find it on the back side.

![i2c Config](/img/i2c-config.jpg)

To configure address of either mcp or temp sensor you have to solder pads in proper order.

## MCP23017 Configuration

| Chip Address | A2       | A1       | A0       | I2C Address |
| ------------ | -------- | -------- | -------- | ----------- |
| 000          |          |          |          | 0x20        |
| 001          |          |          | Soldered | 0x21        |
| 010          |          | Soldered |          | 0x22        |
| 011          |          | Soldered | Soldered | 0x23        |
| 100          | Soldered |          |          | 0x24        |
| 101          | Soldered |          | Soldered | 0x25        |
| 110          | Soldered | Soldered |          | 0x26        |
| 111          | Soldered | Soldered | Soldered | 0x27        |

## Temp Sensor Configuration

| Chip Address | A2       | A1       | A0       | I2C Address | Alternative I2C Address |
| ------------ | -------- | -------- | -------- | ----------- | ----------------------- |
| 000          |          |          |          | 0x18        | 0x48                    |
| 001          |          |          | Soldered | 0x19        | 0x49                    |
| 010          |          | Soldered |          | 0x1A        | 0x4A                    |
| 011          |          | Soldered | Soldered | 0x1B        | 0x4B                    |
| 100          | Soldered |          |          | 0x1C        | 0x4C                    |
| 101          | Soldered |          | Soldered | 0x1D        | 0x4D                    |
| 110          | Soldered | Soldered |          | 0x1E        | 0x4E                    |
| 111          | Soldered | Soldered | Soldered | 0x1F        | 0x4F                    |

## Checking if it works

To check if your configuration works properly you have to use i2cdetect tool

```console
i2cdetect -r -y 2
```

The output ow this command will be like this:

```bash
debian@beaglebone:~$ i2cdetect -y -r 2
     0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f
00:          -- -- -- -- -- -- -- -- -- -- -- -- --
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
20: 20 21 -- -- -- -- -- -- -- -- -- -- -- -- -- --
30: -- -- -- -- -- -- -- -- -- -- -- -- 3c -- -- --
40: -- -- -- -- -- -- -- -- 48 -- -- -- -- -- -- --
50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
60: -- -- -- -- -- -- -- -- 68 -- -- -- -- -- -- --
70: -- -- -- -- -- -- -- --
```
