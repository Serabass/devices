# Host Protocol Version 

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x06`                |
| Code DEC          | `6`                  |
| Implemented on    | BV100, BV20, BV50, COUPON PRINTER, FLATBED PRINTER, NV10USB, NV11, NV12, NV150, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
ITL SSP devices use a system of protocol levels to control the event responses to polls to
ensure that changes would not affect systems with finite state machines unable to test for
new events with non­defined data lengths.

Use this command to allow the host to set which protocol version to operate the slave
device.

If the device supports the requested protocol **OK** **(0xF0)** will be returned.
If not then **FAIL** **(0xF8)** will be returned
# Packet examples

The slave supports the protocol version 8

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 02 06 08 03 94` |
| Slave Reply:   | `7F 80 01 F0 23 80` |


Host protocol version 9 not supported

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 02 06 09 06 14` |
| Slave Reply:   | `7F 80 01 F8 10 00` |

