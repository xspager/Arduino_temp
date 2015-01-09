Get the OneWire lib from http://www.pjrc.com/teensy/arduino_libraries/OneWire.zip

Extract it to ~/sketchbook/libraries/

You will need the package arduino-mk, on Raspian:

$ sudo apt-get install arduino-mk 

Check https://github.com/sudar/Arduino-Makefile for install procedures if you are not using Raspian


Edit the value of BOARD_TAG on Makefile according with the Arduino board you are using


Compile, upload to the board and connect to the seria console

$ export ARDUINO_PORT=/dev/ttyUSB0
$ make upload
$ screen /dev/ttyUSB0
