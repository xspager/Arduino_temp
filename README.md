# Arduino Temp

Outputs the temperature read from DS18B20 to the Arduino's serial console.


## DS18B20 datasheet

http://datasheets.maximintegrated.com/en/ds/DS18B20.pdf

## You will need to 

Get the OneWire lib from http://www.pjrc.com/teensy/arduino_libraries/OneWire.zip

Extract it to ~/sketchbook/libraries/

You will need the package arduino-mk, on Raspian:

```bash
$ sudo apt-get install arduino-mk 
```

Check https://github.com/sudar/Arduino-Makefile for install procedures if you are not using Raspian


## On the hardware side

We are using the pin 10 to talk to the sensor, so, connet it to the middle pin of the sensor and also the VCC and GND pins of the sensor to the ones on the Arduino. Add the required pull-up resistor (of 4.7kohms) between VCC and the output pins.


## Compiling and running it

Edit the value of BOARD_TAG on Makefile according with the Arduino board you are using.

### To compile, upload to the board and connect to the serial console

```bash 
$ export ARDUINO_PORT=/dev/ttyUSB0
$ make upload
$ screen /dev/ttyUSB0
```


## Bluetooth

You can use a Bluetooth module conected to the serial port to get the temperature remotely.
