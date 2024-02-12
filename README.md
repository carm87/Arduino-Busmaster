# Arduino-Busmaster
Arduino as Busmaster CAN Hardware. This sketch works out of box for arduino uno clones devices not equipped with FTDI Usb-serial converter (tested with CH340).
VSCOM official api will try to open any COM port that appear to be named as "USB Serial Port (COMx)" with a baud rate of 3Mbps.
All other real or emulated ports will be opened at 115200.
The sketch works with 115200 and I not yet tried to increase it, I am also not sure Arduino can reach 3Mbps.

I also provided a modified VSCOM dll to be overvritten in the busmaster folder to set 115200 with FTDI chip, too.


1- Upload code for Arduino UNO + CAN-BUS shield (CS PIN 10)

2- Install Busmaster with SER-CAN support, replace dll if you need.

3- BUSMASTER->DRIVER SELECTION->VSCOM ->ADVANCED->SEARCH FOR COM PORT UNTIL YOUR CON APPEAR->OK->OK->CONNECT

The new version also support an i2c SSD1306 display to show status, baudrate and other infos.
