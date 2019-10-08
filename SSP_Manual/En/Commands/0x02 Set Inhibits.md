# Set Inhibits

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x02`                |
| Code DEC          | `2`                  |
| Implemented on    | BV100, BV20, BV50, NV10USB, NV11, NV150, NV200, NV9USB, SMART PAYOUT, SMART SYSTEM |
| Encryption        | **optional**          |

## Description
Sets the channel inhibit level for the device. each byte sent represents 8 bits (channels of
inhibit).

Nv200 has the option to send 2,3,or 4 bytes to represent 16,24, or 64 channels, the other
BNV devices have the option of sending 1 or 2 bytes for 8 or 16 channel operation.

Set the bit low to inhibit all note acceptance on that channel, high to allow note acceptance.

# Packet examples

Set channels 1­3 enabled, 4­16 inhibited

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 03 02 07 00 2B B6` |
| Slave Reply:   | `7F 80 01 F0 23 80` |


All channels enabled

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 03 02 FF FF 25 A4` |
| Slave Reply:   | `7F 80 01 F0 23 80` |

