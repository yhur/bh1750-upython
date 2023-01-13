# bh1750-upython

This project is basically the replica of `https://github.com/PinkInk/upylib/tree/master/bh1750`. 
What I did is

1. copy <a href=https://github.com/PinkInk>PinkInk</a>'s bh1750
2. create a bh1750-upython-mip.json

So anyone who would like to install PinInk's bh1750 library to micoropython environment using `mip` tool, he/she can do it by
```python
import mip
mip.install('github:yhur/bh1750-upython/bh1750-upython-mip.json')
```


And as PinkInk stated, this is how to use this library once installed with the mip following above step.
```python
from machine import Pin, SoftI2C
from bh1750 import BH1750

# init eps8266 i2c
scl = Pin(4)
sda = Pin(3)
i2c = SoftI2C(scl,sda)

s = BH1750(i2c)

while True:
    print(s.luminance(BH1750.ONCE_HIRES_1))
```
