# micro:bit

The micro:bit has several pins, some have predetermined functions.

In general, it can be a good idea that uart (tx/rx) be used on non-analog pins such that the "precious" analog pins are kept clear.

This leaves Pin 8 and Pin 16 as possible candidates.

However, a board should allow for remaping of the pins as application of the micro:bit may mean other pins are used.

## pin out

![microbitpinout](media/microbit_platform_image_2.png)