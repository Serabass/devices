# Get Firmware Version

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x20`                |
| Code DEC          | `32`                  |
| Implemented on    | BV100, BV20, BV50, COUPON PRINTER, FLATBED PRINTER, NV10USB, NV11, NV12, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
Returns a variable length ASCII array containg the full firmware version of the attached
device.

# Packet examples

In this example, the firmware version of the device is: NV02004141498000

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 20 C0 02` |
| Slave Reply:   | `7F 80 11 F0 4E 56 30 32 30 30 34 31 34 31 34 39 38 30 30 30 DE 55` |
| ascii:         | `__ __ __ _. _N _V _0 _2 _0 _0 _4 _1 _4 _1 _4 _9 _8 _0 _0 _0` |

