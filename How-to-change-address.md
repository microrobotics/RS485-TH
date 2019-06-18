**How to change the RS484-TH address**  
The RS485-TH Sensor default slave address is 0x01. In a standard MODBUS network, there is one Master and up to 247 Slaves, each with a unique Slave Address from 1 to 247. The Master can also write information to the Slaves. The following procedure describe how to change the device address. 

**Important Note**  
- When changing the address, there can be only one slave device on the bus, otherwise all slave devices will be changed.
- When the address is change, the CRC checksum must be recalculated. See document How to Calculating CRC checksum - https://github.com/microrobotics/RS485-TH/blob/master/How-to-calculate-CRC-checksum.md



