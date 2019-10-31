Pytilt
==========
Tool for reading your Tilt brewing hydrometer[1] in python on a rasberry pi and send the data to a server.


Installation
------------
0. git clone https://github.com/atlefren/pytilt.git
1. Install python-bluez: ```sudo apt-get install python-bluez```
2. Make the bluetooth interface accessible witout being root: ```sudo setcap cap_net_raw+eip /usr/bin/python2.7```

Running
-----------
0. From the directory containing pytilt.py run `python pytilt.py`

Running Pytilt in the background and on System Start
-----------
0. edit pytilt.service, add your key and fix paths
1. copy pytilt.service to /lib/systemd/system/
2. sudo chmod 644 /lib/systemd/system/pytilt.service
3. sudo systemctl daemon-reload
4. sudo systemctl enable pytilt.service
5. sudo reboot


Acknowledgements
----------------
The code in blescan-py is adapted from https://github.com/switchdoclabs/iBeacon-Scanner-
The Tilt UUID-to-color mapping is taken from: https://github.com/tbryant/brewometer-nodejs
Systemd-config here: http://www.raspberrypi-spy.co.uk/2015/10/how-to-autorun-a-python-script-on-boot-using-systemd/


[1]: https://tilthydrometer.com/
