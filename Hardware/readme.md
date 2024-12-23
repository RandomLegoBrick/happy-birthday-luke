# List of datasheets, Tutorial Aricles, 
I'm sure there are better tutorials and libraries available. These are simply the ones I used. Just google search the names of each parth with "micropython" appended on, and you will find plenty of resources.

## (Microcontroller) Raspberry Pi Pico
Datasheet: https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf <br>
Tutorials: https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico, https://www.raspberrypi.com/documentation/microcontrollers/micropython.html <br>

## (IMU) MPU-6050

Datasheet: https://invensense.tdk.com/wp-content/uploads/2015/02/MPU-6000-Datasheet1.pdf <br>
Micropython Library Used: https://github.com/Lezgend/MPU6050-MicroPython
(Modified Line 73 of MPU6050.py to `self.i2c = SoftI2C(scl=Pin(27), sda=Pin(26), freq=100000)`)

## (Display) ST7789 240x320 2 Inch LCD

ST7789 Datasheet: <br>
LCD Tutorial: https://www.waveshare.com/wiki/2inch_LCD_Module <br>
Micropython Library Used: https://github.com/russhughes/st7789_mpy/tree/master