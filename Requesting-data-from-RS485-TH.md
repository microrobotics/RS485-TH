**How to request Data from the Sensor, default address 0x01** 

- Request Data = 01 03 00 00 00 02 C4 0B (Hex, 8 Bytes)
- Data Returned from sensor = 01 03 04 01 11 02 72 2A 8F (Hex, 9 Bytes)

**Request Data Format**
- 01 : Address
- 03 : Mode - Read 
- 00 : na
- 00 : na
- 00 : na
- 02 : No of registers requested 
- C4 : CRC16 Checksum - Lo Byte 
- 0B : CRC16 Checksum - High Byte

Please note, if any changes are made to the address, command or data field, the CRC-16 checksum must be re calculated (see down below for instructions)

**Return Data Format**
- 01 : Address
- 03 : Mode - Read was done
- 04 : Data Lenght - 4 Bytes
- 01 : Temp Hi Byte
- 11 : Temp Low Byte
- 02 : Humidity Hi Byte
- 72 : Humidity Low Byte
- 2A : CRC16 Low Byte
- 8F : CRC16 High Byte

**How to extract Temperature and Humidty from return data**
**Tempature**

- 01 : Temp Hi Byte
- 11 : Temp Low Byte
- 0111 (Hex) = 273 (DEC) = 27.3°C 

**Humidity**
- 02 : Humidity Hi Byte
- 72 : Humidity Low Byte
- 0272(Hex) = 626(Dec) = 62.6% 





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






