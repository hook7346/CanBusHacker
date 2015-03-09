# CanBusHacker
This is a project to make a real time CAN packet monitoring system using Arduino and CAN BUS shield hardware. This makes a very affordable and reliable CAN packet monitor and injector.

## Prerequisites
### Hardware
* Arduino UNO
* CAN BUS Shield: Currently this project supports Can Bus Shield v1.1 product (http://www.jayconsystems.com/can-bus-shield.html). You can also purchase this from eBay.
  
  We will add support for other products as we have access to them

* OBD-II to DB9 Cable: something similar to this https://www.sparkfun.com/products/10087
* USB to PC Cable to program and transfer serial data to and from Arduino

### Software
* Python 2.7.x: http://python.org
* Pyside: https://pypi.python.org/pypi/PySide (pip install pyside)
* PySerial: https://pypi.python.org/pypi/pyserial (pip install pyserial)

### How to Install
##Program Arudino
* Download Arduino Library from CanBusShield's vendor site. For example, for JayConSystems product, I could download it from http://www.jayconsystems.com/fileuploader/download/download/?d=0&file=custom%2Fupload%2FFile-1363136372.zip. But, you need to modify the code to gather raw packets. The CANBridge\JS-3486 folder contains the library for JayCon product. It has some modifications in the code to support raw level packet collection. If you want to support your board, you should go through similar code change.
* Next, import the library using the method described here: http://arduino.cc/en/guide/libraries
* Open CanBridge.ino file, compile and upload to your device

##CanBusHacker.py
This program is for Windows program that communicates with Arduino board through serial port. Install dependencies and run CanBusHacker.py. Select Arduino -> Start Capture menu. You need to select serial port that is connected to your Aruino and need to specify output database file. The database file format is SQLite and you can open it up later using File -> Open Log menu.
