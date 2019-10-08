# Reset

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x01`                |
| Code DEC          | `1`                  |
| Implemented on    | BV100, BV20, BV50, COUPON PRINTER, FLATBED PRINTER, NV10USB, NV11, NV12, NV150, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
Performs a software and hardware reset of the device.

After this command has been acknowledged with OK (0xF0), any encryption, baud rate
changes, etc will be reset to default settings.

# Packet examples

No data parameters, sequence bit set and address 0

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 01 06 02` |
| Slave Reply:   | `7F 80 01 F0 23 80` |

