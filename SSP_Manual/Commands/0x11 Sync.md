# Sync

|                   |                       |
|:-----------------:|:---------------------:|
| Code HEX          | `0x11`                |
| Code DEC          | `17`                  |
| Implemented on    | BV100, BV20, BV50, COUPON PRINTER, FLATBED PRINTER, NV10USB, NV11, NV12, NV150, NV200, NV9USB, SMART HOPPER, SMART PAYOUT, SMART SYSTEM, SMART TICKET |
| Encryption        | **optional**          |

## Description
SSP uses a system of sequence bits to ensure that packets have been received by the slave
and the reply received by the host. If the slave receives the same sequence bit as the
previous command packet then this is signal to re­transmit the last reply.

A mechanism is required to initially set the host and slave to the same sequence bits and
this is done by the use of the SYNC command.

A **SYNC** command resets the seq bit of the packet so that the slave device expects the next
seq bit to be 0. The host then sets its next seq bit to 0 and the seq sequence is
synchronised.

The **SYNC** command should be the first command sent to the slave during a session.

# Packet examples

Set seq bit to 1


|                |                     |
|---------------:|:--------------------|
| Host transmit: | `7F 80 01 11 65 82` |
| Slave Reply:   | `7F 80 01 F0 23 80` |

