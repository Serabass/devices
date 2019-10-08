# Uint Data

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x0D`                |
| Code DEC          | `13`                  |
| Implemented on    | BV100, BV20, BV50, NV10USB, NV11, NV150, NV200, NV9USB, SMART PAYOUT |
| Encryption        | **optional**          |

## Description
A command to return version information about the connected device to the format
described in the table below:

| byte offset | function                                    | size |
|:-----------:|:-------------------------------------------:|:----:|
| 0           | Generic OK Response (OxF0)                  | 1    |
| 1           | Unit type: see Uint Type Table for codes    | 1    |
| 2           | Firmware version (4 byte ASCII)             | 4    |
| 6           | Dataset country (3 byte ASCII)              | 3    |
| 9           | Value multiplier                            | 3    |
| 12          | Protocol version                            | 1    |


# Packet examples
This is a response example for a banknote validator EUR 5,10,20 version 3.00 protocol version
7

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 0D 2E 02`   |
| Slave Reply:   | `7F 80 0D F0 00 30 33 30 30 45 55 52 01 00 00 07 01 85`   |
| ascii:         | `__ __ __ _. _. _0 _3 _0 _0 _E _U _R _. _. _. _.`   |
