# MicroPython port for L3G4200D


![alt text](https://github.com/kriddaw/L3G4200D/raw/master/gy50_repl.png)


----
## 3 Axis Gyro
I used a couple existing scripts for arduino and raspi to put together this class. As you can see it outputs a dict of the xyz values of the sensor.

----
## Usage

Instantiate I2C device, scan bus for i2c address, instantiate gyro object, run xyz_values method. Create loop to stream data.

```python
from machine import Pin, I2C
from gy50 import GY50
i2c = I2C(scl=Pin(22), sda=Pin(21))
i2c.scan()
>>> [105]
address = 105
gyro = GY50(i2c, address)
gyro.xyz_values()
>>> {'x': -1.8, 'y': -0.5, 'z': 0.0}
```
