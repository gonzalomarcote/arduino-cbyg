# arduino-cbyg
Arduino project to display in one LCD data from serveral sensor from an MQTT broker.

### Arduino project to display in one LCD personal info
Arduino Uno board project that shows in an LCD the rack and some servers termperature.  
Optionally I will recollect another personal info from another sources and projects (surf tide, waves, etc).  
Compiled with `arduino-mk` linux package.  

`sketch.ino` -> is the main program file.  
`Makefile` -> the make file to compile it with arduino-mk.  

The following libraries need to be downloaded to `/usr/share/arduino/libraries/`:
* Wire
* WiFi
* SPI
* Time
* TimeAlarms
* Timezone

To upload `skecth.ino` sketch to arduino uno board just type:
```
$ fuser -k /dev/ttyACM0
$ make upload
```
Be sure to be in `dialout` group.  

To connect to serial type:  
```
$ screen /dev/ttyACM0 115200
```
Be sure to have in `Serial.begin(115200)` the same serial number. 
