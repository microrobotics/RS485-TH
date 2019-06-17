## RS485-TH
Modbus RS485 Temperature and Humidity Sensor

The RS484-TH sensor is based on the SHTXX series high accuracy Temperature and Humidity Series of sensors and offer  Modbus RS484 communication. Most of the manufacturer documentation is still in Chinese and this webpage will be updated with information as it becomes available.

**Specifications** 

- Working voltage: 9-36V
- Maximum power: 0.3W
- Operating temperature: -20 ℃ to +60 ℃, humidity 0% RH-80% RH
- Accuracy: Temperature ± 0.3 ℃ (25 ℃), humidity ± 3% RH (25 ℃)
- Output interface: RS485 (standard MODBUS protocol)
- Device address: can be set to 1-255, the default is 1
- Baud rate: 9600, 8 bits of data, 1 stop, no parity
- Size: 60 * 30 * 18mm
- Product Link https://www.robotics.org.za/RS485-TH

**Pinouts**

- +V = Yellow
- GND = Black
- RED = 485-A
- GREEN = 485-B

**Serial Setting**

- Baud rate: 9600, 8 bits, 1 stop, no parity
- Default Slave Address = 01

**Terminal Program**
- Any terminal program that supprt Hex can be used, but Accessport works great and is free 
- Download at http://www.sudt.com/en/ap/index.html

**Modbus & RS485 Relationship**

A MODBUS master message to the slave is made up from 8 bytes that contains the slave address, a command, the data, and a CRC check sum.
Since Modbus protocol is just a messaging structure, it is independent of the underlying physical layer. It is traditionally implemented 
using RS485, RS422 or RS232.  



