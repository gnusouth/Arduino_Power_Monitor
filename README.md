Arduino Power Monitor
=====================

A simple program to monitor the serial output of a CurrentCost 128 power meter and send the data to 
ThingSpeak using an Arduino.

## About

Updated by Michael Sproul for use with Thingspeak and the Python based CLI build tool, `ino`. Based on 
[original code](https://github.com/bleep1/CurrentCostToCosmViaArduino) by Brian Lee (bleep1)

## Parts List

1. Current Cost 128 power monitor.  http://www.currentcost.com/product-envi.html I got mine from: 
http://www.smartnow.com.au/
2. Arduino.  I used an Etherten from Freetronics. http://www.freetronics.com/products/etherten
3. Home made serial cable, RJ45->Arduino. Blue = Ground, Brown = Monitor output/Arduino input
4. Login account at http://www.thingspeak.com
5. This GIT repo
7. Ino from http://inotool.org/

## Libraries

Since changing from Xively to ThingSpeak, no extra libraries are required!

## Building

Add your ThingSpeak API key in the necessary place(s), modify ino.ini to reflect the Arduino you've 
got, and run `ino build && ino upload && ino serial`.

You can also edit `~/.inorc` to set your Ino preferences globally.

## Testing

If you want to test your setup without parsing the data or uploading it to ThingSpeak you can build and 
run the project in the serial-test directory. Run `ino build && ino upload && ino serial` from the 
serial-test directory and you'll see the XML output from the meter (hopefully).

## Reference material

* Info on the data from the Cust Cost serial port: http://www.currentcost.com/download/Envi%20XML%20v19%20-%202011-01-11.pdf
* Another guy who did something similar: http://mungbean.org/blog/?p=477
