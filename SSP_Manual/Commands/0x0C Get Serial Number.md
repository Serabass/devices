# Get Serial Number

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x0C`                |
| Code DEC          | `12`                  |
| Implemented on    | BV100, BV20, BV50, COUPON PRINTER, FLATBED PRINTER, NV10USB, NV11, NV12, NV150, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
This command returns a 4­byte big endian array representing the unique factory
programmed serial number of the device.

# Packet examples

The device responds with 4 bytes of serial number data. In this case, the serial number is
01873452 = 0x1c962c. The return array is formatted as big endian (MSB first).


|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 0C 2B 82` |
| Slave Reply:   | `7F 80 05 F0 00 1C 96 2C D4 97` |

