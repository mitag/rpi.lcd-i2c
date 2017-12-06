I2C LCD Python driver
==================================
Python library for accessing character LCDs from a Raspberry Pi or other Pi like SBCs.



For all plattforms, make sure you have the following dependencies:
````
sudo apt-get update
sudo apt-get install build-essential python-dev python-smbus i2c-tools python-pip git
````
Add your user to the i2c group::
````
sudo adduser pi i2c
````
Then reboot.
````
sudo reboot
````
Now check that the I2C LCD is communicating properly and which address it uses.
````
i2cdetect -y 1
     0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f
00:          -- -- -- -- -- -- -- -- -- -- -- -- -- 
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
20: -- -- -- -- -- -- -- 27 -- -- -- -- -- -- -- -- 
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
40: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
70: -- -- -- -- -- -- -- -- 
````
Installing the Python Package
-----------------------------
````
git clone https://github.com/mitag/rpi.lcd-i2c.git
cd rpi.lcd-i2c/
sudo python setup.py install
````
