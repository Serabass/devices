# Enable

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x0A`                |
| Code DEC          | `10`                  |
| Implemented on    | BV100, BV20, BV50, COUPON PRINTER, FLATBED PRINTER, NV10USB, NV11, NV12, NV150, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
This command will enable the SSP device for normal operation. For example, it will allow a
banknote validator to commence validating banknotes entered into it's bezel.

# Packet examples

Single byte command with no parameters

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 0A 3F 82` |
| Slave Reply:   | `7F 80 01 F0 23 80` |

NV11 when note float is jammed/disconnected responds COMMAND_CANNOT_BE_PROCESSED

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 0A 3F 82` |
| Slave Reply:   | `7F 80 01 F5 3D 80` |

