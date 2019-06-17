**RS485-TH CRC-16 Checksum Background**  
When data is send to or from the RS485-TH sensor the last 2 bytes represent the checksum. 

**Example - Request Data**
- 01 03 00 00 00 02 C4 0B   
- C4 : CRC16 Checksum - Lo Byte
- 0B : CRC16 Checksum - High Byte
- Checksum = 0x0BC4

*So for the default address the checksum is given by the manufacturer*


