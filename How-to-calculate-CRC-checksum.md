**Checksum Background**  
A MODBUS master message to the slave is made up from 8 bytes that contains the slave address, a command, the data, and a CRC check sum. The checksum is calculated based on the values of the address, command and the data. Whenever these values change, the chacksum must be recalculated. The last 2 bytes represent the checksum. 

**Example - Request Data**
- 01 03 00 00 00 02 C4 0B   
- C4 : CRC16 Checksum - Lo Byte
- 0B : CRC16 Checksum - High Byte
- Checksum = 0x0BC4
- Usually the checksum is for the default address and we do not need to calculate it
- If we make changes to the address, command or data, the checksum must be recalculated 

**How to calculate the CRC Checksum with online CRC Calculator**
- Go to https://www.lammertbies.nl/comm/info/crc-calculation.html  
- Select Hex Format  
- Insert Request Data (without CRC) into the CRC calculater for - eg 010300000002  
- Calculate -> Output CRC-16 (Modbus) =	0x0BC4





