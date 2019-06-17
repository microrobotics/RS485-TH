**How to read Data from the Sensor** 

Modbus request consist of a 8 Byte Header. 

Slave ID (2 bytes) | Command(2 bytes) | Data (4 bytes) | CRC (4 bytes)
|:--------:|:--------:|:-------:|:---------:|
 |  XX    |   XX  |  XX XX  | CL CH |

**Example**
Send Hex Data 01 03 00 00 00 02 C4 0B

- 01 - Slave Address
- 03 - Read (Mode 03)
- 00
- 00 
- 00 
- 02 - No of Registers Requested
- XX - CRC16 Checksum To be calculated - Lo Byte 
- XX - CRC16 Checksum To be calculated - High Byte

**Online CRC Calculator**

Any online CRC calculator that can calculate CR16 Modbus can be used
- Go to https://www.lammertbies.nl/comm/info/crc-calculation.html
- Select Hex Format
- Insert data crc to be calculated for - eg 010300000002 
- Calculate -> Output CRC-16 (Modbus) =	0x0BC4

**Final Request with CRC looks like this - Please note order of CRC Low and High Byte** 

Send Hex Data 01 03 00 00 00 02 C4 0B







