# Display Off

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x04`                |
| Code DEC          | `4`                  |
| Implemented on    | BV100, BV20, BV50, NV10USB, NV11, NV150, NV200, NV9USB, SMART PAYOUT |
| Encryption        | **optional**          |

## Description
Allows the host to control banknote validator bezel illumination. Use this command to
disable illumination whne the validator is enabled for note entry.

# Packet examples

Single byte command with no parameters

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 04 18 02` |
| Slave Reply:   | `7F 80 01 F0 23 80` |
