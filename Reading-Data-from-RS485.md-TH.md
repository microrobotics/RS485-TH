**How to read Data from the Sensor** 

Modbus request consist of a 8 Byte Header 

Slave ID (2 bytes) | Command(2 bytes) | Data (4 bytes) | CRC (4 bytes)
|:--------:|:--------:|:-------:|:---------:|
 |  XX    |   XX  |  XX XX  | XX XX |

**Example**
Send Hex Data 01 03 00 00 00 02 C4 0B

- 01 - Slave Address
- 03 - Read (Mode 03)
- 00
- 00 
- 00 
- 02 - No of Registers Requested
- C4 - CRC16 Checksum - Lo Byte 
- 0B - CRC16 Checksum - High Byte

**How to calculate CRC16 Checksum**

Data to be send withot Checksum at the end -> 010300000002 






