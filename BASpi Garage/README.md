# Universal Devices Garage Door(s) Controller v3

* This is a WiFi Controlled Garage door opener momentary push button duplicator, with optional local camera.

## Garage Doors, utilizing Contemporary Controls BASpi-6u6r Device

* The purpose of this Polyglot Node Server is to command the door or doors Open, Closed or Bumped Opened. With Open, Close and Stopped as Statuses for 1 all the way up to 6 Garage Doors. The Door Command, Door will Open if closed and Close if opened with a 15 second delay for Status in between. Bump is just like the override button in your garage or remote you can stop the door anywhere in its travel. The delay between status is also so, no garage door will run together, if more than one garage door is installed. Please note that multiple pushes will lead to multiple starts and stops with 15 seconds in between Enable and no delay for Bump!, so only press once then wait for status feedback of OPEN, CLOSED or STOPPED is populated on your ISY administrator console or your phone app. Bump is to partially open the Garage Door Open and it will show Stopped for status, if travel is full open or closed it will show up on a refresh. Use at your own risk and follow all safety guild lines and local codes for external low voltage devices.
* This Network series will include in the near future custom home control for Irrigation, Pool Control, Well Pump Control, General HVAC control, VVT, Boiler, Chiller along with any custom control you create utilizing the released bascontrolns module.

[bascontrolns](https://pypi.org/project/bascontrolns/)

## Based on the Contemporary Controls BASpi6U6R Device

![BASpi 6U6R Network Poly](https://github.com/sjpbailey/udi-poly-basgarage-python-master-v3/blob/master/Images/Class_nodses_garage_door.png)

* Doors 1-6 you can use the controller for one, two, three or all the way up to 6 doors.

![BASpi 6U6R One](https://github.com/sjpbailey/udi-poly-basgarage-python-master-v3/blob/master/Images/Controller_garage_doors.png)

### BASpi-SYS6U6R DIY BacNet Control Device by Contemporary Controls

* It utilizing the Contemporary Controls BASpi SYS6U6R control Device.
Please Visit these links for information & configuration of this Device.

[Contemporary Controls BASpi DIY](https://www.ccontrols.com/basautomation/baspi.php)

* BASpi 6U6R Controller
[Contemporary Controls BASpi 6U6R](https://www.ccontrols.com/pdf/ds/BASPI-datasheet.pdf)
* BASpi 6U6R Installation
[Contemporary Controls BASpi 6U6R Install](https://www.ccontrols.com/pdf/BASpi-hardware-install-guide.pdf)
* BASpi 6U4R2A Controller
[Contemporary Controls BASpi 6U4R2A](https://www.ccontrols.com/pdf/ds/BASPI-AO2-datasheet.pdf)
* BASpi 6U4R2A Installation
[Contemporary Controls BASpi 6U4R2A Install](https://www.ccontrols.com/pdf/TD180600.pdf)
* BASpi Controller Configuration
[Contemporary Controls BASpi Configuration Quick Start](https://www.ccontrols.com/pdf/is/BASPI-QSGuide.pdf)

#### Camera On Controller

* BASpi-6U6R is hosted by a Raspberry pi, you can add a USB camera to the RPi and run VLC Media Player. Then utilize the VNC viewer to pipe it out to your network.
* This controller sits on a Raspberry Pi. You can easily add it to your ISY after you configure its ip address in your configuration page in Polyglot.

* Please see the YouTube video below, you have to configure the BASpi6U6R devices Inputs for Resistance, Type & COV (change of value increment, this keeps the transmitted resistor values from bouncing).

[Universal Input Configuration for the Garage Door Node Server Video](https://youtu.be/I3tSfYk8ti8)

* A 5.6k ohm resistor is added to the open switch and a 12k ohm resistor to the close switch, both on one leg of the switch to the wire so when the switch is closed it sees the resistance.

[Resistor Installation: Review with Door, IOS App and Camera Testing](https://youtu.be/mVyMzNkizIs)

![Resistor Installation: CAD Drawing](https://github.com/sjpbailey/udi-poly-basgarage-python-master-v3/blob/master/Images/CAD_Wiring.png)

![Input Configuration](https://github.com/sjpbailey/udi-poly-basgarage-python-master-v3/blob/master/Images/shot_3.png)

![Installed Example Device](https://github.com/sjpbailey/udi-poly-basgarage-python-master-v3/blob/master/Images/IMG_2082.jpg)

![Installed Example Camera](https://github.com/sjpbailey/udi-poly-basgarage-python-master-v3/blob/master/Images/IMG_2081.jpg)

* Requirments
* Python 3.7.7
* bascontrolns>=0.0.3
* udi_interface>=3.0.8
* requests
* urllib3

* Supported Nodes
* Six 6 Universal Inputs
* Six 6 Binary Outputs

##### Configuration Example

![Paramerter Input Example](https://github.com/sjpbailey/udi-poly-basgarage-python-master-v3/blob/master/Images/basgarage-Key.png)

##### Defaults

* Default Short Poll:  Every 1 minutes
* Default Long Poll: Every 4 minutes

###### User Provided

* Enter your IP address for your BASpi-SYS6U6R controller,
* key = door_ip
* Value = Enter Your BASpi IP Address.

* Save and restart the NodeServer
