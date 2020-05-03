# MicroPython port for L3G4200D


![alt text] (https://github.com/kriddaw/L3G4200D/raw/master/gy50_repl.png)


----
## 3 Axis Gyro
I used a couple existing libraries for arduino and raspi to put together this class. As you can see if outputs a dict of the xyz coordinates of the sensor.

----
## Usage

Instantiate I2C device, scan bus for i2c address, instantiate gyro object, run xyz_values method.

'''python
from machine import Pin, I2C
from gy50 import GY50
i2c = I2C(scl=Pin(22), Pin(21))
address = 105
gyro = GY50(i2c, address)
gyro.xyz_values()
'''
