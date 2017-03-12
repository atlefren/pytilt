Pytilt
==========
Tool for reading your Tilt brewing hydrometer[1] in python on a rasberry pi and send the data to a server.


Installation
------------
0. git clone https://github.com/atlefren/pytilt.git
1. Install pyhton-bluez: ```sudo apt-get install python-bluez```
2. Make the bluetooth interface accessible witout beeing root: ```sudo setcap cap_net_raw+eip /usr/bin/python2.7```
3. edit pytilt.service, add your key and fix paths
4. copy pytilt.service to /lib/systemd/system/
5. sudo chmod 644 /lib/systemd/system/pytilt.service
6. sudo systemctl daemon-reload
7. sudo systemctl enable pytilt.service
8. sudo reboot


2. sudo python log.py


Acknowledgements
----------------
The code in blescan-py is adapted from https://github.com/switchdoclabs/iBeacon-Scanner-
The Tilt UUID-to-color mapping is taken from: https://github.com/tbryant/brewometer-nodejs
Systemd-config here: http://www.raspberrypi-spy.co.uk/2015/10/how-to-autorun-a-python-script-on-boot-using-systemd/


[1]: https://tilthydrometer.com/