This is a port of the RFM69 library for arduino from https://github.com/LowPowerLab/RFM69 to python for raspberry pi.
Attach the RFM69 as follows (slight change from etrombly's default for use with redbear IOT phat which uses pin 18):

| RFM pin | Pi pin    | Pi GPIO  |
| --------|:---------:|:-----:|
| 3v3     | 17        |    |
| MOSI    | 19        | 10  |
| MOSI    |  21       | 9 |
| CLK     | 23        |11|
| NSS     | 24        | 8 |
| GND     | 25        | |
|RESET    | 29        |   5 |
| DIO0    | 33        |  13  |

You can change the interrupt pin (GPIO13) in the class init.  

prerequisites: RPi.GPIO and spidev

if you are using newer firmware you'll need to get a newer spidev, the old one is no longer working:

git clone https://github.com/Gadgetoid/py-spidev

cd py-spidev

sudo make install
