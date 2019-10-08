# Disable

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x09`                |
| Code DEC          | `9`                  |
| Implemented on    | BV100, BV20, BV50, COUPON PRINTER, FLATBED PRINTER, NV10USB, NV11, NV12, NV150, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
Disabled the slave device from operation.

For example, this command would block a banknote validator from allowing any more
banknotes to be entered.

For most SSP devices, the default state is to be disabled after reset.

# Packet examples

Single byte command with no parameters

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 09 35 82` |
| Slave Reply:   | `7F 80 01 F0 23 80` |


NV11 when note float is jammed/disconnected responds COMMAND_CANNOT_BE_PROCESSED

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 09 35 82` |
| Slave Reply:   | `7F 80 01 F5 3D 80` |

