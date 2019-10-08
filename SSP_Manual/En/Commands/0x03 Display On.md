# Display On

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x03`                |
| Code DEC          | `3`                  |
| Implemented on    | BV100, BV20, BV50, NV10USB, NV11, NV150, NV200, NV9USB, SMART PAYOUT |
| Encryption        | **optional**          |

## Description
Allows the host to control the illumination of the bezel. Send this command to show bezel
illumination when the device is enabled for banknote validation. (This is the default
condition at reset).

Note that the validator will still override the illumination of the bezel,
i.e. the bezel will **not** be illuminated if the device is **not enabled**
even if this command is sent.

# Packet examples

Single byte command with no parameters.

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 03 09 82` |
| Slave Reply:   | `7F 80 01 F0 23 80` |
