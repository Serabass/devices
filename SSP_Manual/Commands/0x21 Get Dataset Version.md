# Get Dataset Version

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x21`                |
| Code DEC          | `33`                  |
| Implemented on    | BV100, BV20, BV50, NV10USB, NV11, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM |
| Encryption        | **optional**          |

## Description
Returns a varibale length ASCII array giving the installed dataset version of the device.

# Packet examples
This example shows a device with dataset version EUR01610.

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 21 C5 82` |
| Slave Reply:   | `7F 80 09 F0 45 55 52 30 31 36 31 30 B8 2A` |
| ascii:         | `__ __ __ _. _E _U _R _0 _1 _6 _1 _0` |

