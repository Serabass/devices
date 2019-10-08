# Poll

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x07`                |
| Code DEC          | `7`                  |
| Implemented on    | BV100, BV20, BV50, COUPON PRINTER, FLATBED PRINTER, NV10USB, NV11, NV12, NV150, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
This command returns a list of events occured in the device since the last poll was sent.

The SSP devices share some common events and have some unique events of their own.
See event tables for details for a specific device.

# Packet examples

Poll command returning device reset and disabled response

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 07 12 02` |
| Slave Reply:   | `7F 80 03 F0 F1 F8 DC 0C` |

Event response note credit channel 1 and note stacked

|                |                       |
|---------------:|:----------------------|
| Host transmit: | `7F 80 01 07 12 02` |
| Slave Reply:   | `7F 80 04 F0 EE 01 EB B9 48` |

