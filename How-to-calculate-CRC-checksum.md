**RS485-TH CRC-16 Checksum Background**  
When data is send too or from the RS485-TH sensor the last 2 bytes represent the checksum. 

**Example - Request Data**
- 01 03 00 00 00 02 C4 0B   
- C4 : CRC16 Checksum - Lo Byte
- 0B : CRC16 Checksum - High Byte
- Checksum = 0x0BC4

*So for the default address the checksum is given by the manufacturer, we can actually check if this is correct by using an online CRC Calculator*

- Go to https://www.lammertbies.nl/comm/info/crc-calculation.html  
- Select Hex Format  
- Insert Request Data (without CRC) into the CRC calculater for - eg 010300000002  
- Calculate -> Output CRC-16 (Modbus) =	0x0BC4

**So why is their a need to calculate the CRC Checksum**  




