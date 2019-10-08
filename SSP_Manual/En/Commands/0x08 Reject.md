# Reject

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x08`                |
| Code DEC          | `8`                  |
| Implemented on    | BV100, BV20, BV50, NV10USB, NV11, NV150, NV200, NV9USB, SMART PAYOUT |
| Encryption        | **optional**          |

## Description
After a banknote validator device reports a valid note is held in escrow, this command may
be sent to cause the banknote to be rejected back to the user.

# Packet examples

Single byte command with no parameters

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 08 30 02` |
| Slave Reply:   | `7F 80 01 F0 23 80` |
