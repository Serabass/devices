# Setup Request

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x05`                |
| Code DEC          | `5`                  |
| Implemented on    | BV100, BV20, BV50, FLATBED PRINTER, NV10USB, NV11, NV12, NV150, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
Request the set­up configuration of the device. Gives details about versions, channel
assignments, country codes and values.

Each device type has a different return data format. Please refer to the table information for
each individual device.

## SMART Ticket/Coupon Printer Response

| Smart Ticket Data | Response Offset | Size | Notes |
|:-----------------:|:---------------:|:----:|:-----:|
| Unit Type                         | 0  | 1 | 0x08 = SMART Ticket, 0x0B = Coupon Printer |
| Firmware Version                  | 1  | 4 | Ascii data of device firmware (eg 0123) |
| Cutter Enabled                    | 5  | 1 | (0 for disabled) |
| Tab enabled status                | 6  | 1 | (0 for disabled) |
| Reverse validation enabled status | 7  | 1 | (0 for disabled) |
| Font pack code (ASCII)            | 8  | 3 | e.g. FP1 |
| Printer type                      | 11 | 1 | Printer Type: 0x0 for Fan Fold, 0x1 Paper Roll (Cutter fitted) |
| SD card fitted status             | 12 | 1 | (1 for detected) |
| Printer darkness/quality setting  | 13 | 1 | value between 0 ­ 3 |
| SSP Protocol Version              | 14 | 1 | |

## Packet examples

This example shows the data returned for a BNV with GBP dataset, firmware version 1.00, 3
channels GBP 5, GBP 10, GBP 20

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 05 1D 82` |
| Slave Reply:   | `7F 80 17 F0 00 30 31 30 30 47 42 50 00 00 01 03 05 0A 14 02 02 02 40 00 00 05 61 81` |
| ascii:         | `__ __ __ _. _. _0 _1 _0 _0 _G _B _P _. _. _. _. _. _. _. _. _. _. _@ _. _. _.` |
