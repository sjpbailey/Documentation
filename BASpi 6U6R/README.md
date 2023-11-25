# Universal Devices WiFi IP NodeServer

## Manufacturer Contemporary Controls, WiFi Bacnet IP Control Devices

## BASpi-6U6R and or the BASpi-Edge-SYS6U6R BACnet/IP WiFi/IP

* These controller(s) can be used to control low voltage switchable external devices. Use a Relay interface for any advanced control sequence attached via ethernet or WiFi IP.

## Reasons

* The purpose of this Nodeserver is for conventional control of low voltage systems 24vac or less (relays). Custom control through the ISY for general Home automation for multiple control operations, WiFi, IP, BACnet.

* It utilizes Contemporary Controls BASpi-6U6R or the BASpi-Edge-6U6R BACnet WiFi IP control Modules.

* Have more than one Device? Just edit the parameter "key" nodes value to match the number of devices you have, then for each BASpi-6u6r added you will then need to add the IP Address for "value" to match each BASpi-6u6r controller, ip_1-6 is already in the key just add your IP Address(es).

* You can add up to six (6) controllers or nodes with this node serer.

* All switching is 24vac or lower for all outputs on the Edge or BASpi-6u6r device! Edge Device has two common buss terminals linked to outputs refer to installation.

* ALL OUTPUTS ARE LOW VOLTAGE 24VAC OR LESS, USE THE APPROPRIATE INTEFACE RELAY FOR SWITCHING ABOVE 24VAC!!

* Please see links below for information & configuration of this Device within Contemporary Controls GUI.
Typical pool wiring diagram below, used with BASPOOL Node Server.

* This Network BAS series will include in the near future custom home control for Garage Door, Well Pump Control, HVAC, VVT, Boiler, along with any custom control you create utilizing the pip bascontrolns module <https://pypi.org/project/bascontrolns/>.

* This controller sits on a Raspberry Pi. You can easily add it to your ISY after you configure its IP address.

![CAD Wiring Example](https://github.com/sjpbailey/udi-poly-baspi-6u6r-python-master-v3/blob/93fcde3c76b8d4da4c819d8b5ce47a0b8e15e041/Archive-images/Pool-CAD.png)

### BASpi-SYS6U6R and the BASpi-Edge DIY BacNet Control Device by Contemporary Controls

* Main
[Contemporary Controls BASpi DIY](https://www.ccontrols.com/basautomation/baspi.htm)
* BASpi Controller Configuration
[Contemporary Controls BASpi Configuration Quick Start](https://www.ccontrols.com/pdf/is/BASPI-QSGuide.pdf)
* BASpi 6U6R Controller
[Contemporary Controls BASpi Edge 6U6R](https://www.ccontrols.com/basautomation/baspiedge.php)
* BASpi 6U6R Controller
[Contemporary Controls BASpi 6U6R](https://www.ccontrols.com/pdf/ds/BASPI-datasheet.pdf)
* BASpi 6U6R Installation
[Contemporary Controls BASpi 6U6R Install](https://www.ccontrols.com/pdf/BASpi-hardware-install-guide.pdf)
* BASpi 6U4R2A Controller
[Contemporary Controls BASpi 6U4R2A](https://www.ccontrols.com/pdf/ds/BASPI-AO2-datasheet.pdf)
* BASpi 6U4R2A Installation
[Contemporary Controls BASpi 6U4R2A Install](https://www.ccontrols.com/pdf/TD180600.pdf)

#### Input Configuration

* You must configure your inputs for the appropriate end devices attached to your inputs, this is done by calling the controllers IP Address from your browser.

[Universal Input Configuration Video](https://www.youtube.com/watch?v=hTd1mR7npP4)

* Python 3.8

* Supported Nodes
  * Up to 36 Universal Inputs
  * Up to 36 Binary Outputs
  
##### Configuration

###### Defaults

* Default Short Poll:  Every 120 seconds
* Default Long Poll: Every 4 minutes (heartbeat)

###### Requirements

* requests
* bascontrolns >= 0.0.3
* udi_interface

###### User Provided

* Enter the number of pool nodes you desire 0-6
* Enter your IP address for up to six (6) BASpi-SYS6U6R controller,
* Config: key = nodes this parameter is provided, Value = (* = 1-6)
* Config: key = ip_* (* = 1-6) this value is provided, Value = Enter Your BASpi IP Address, Example: key ip_1  value 192.168.1.47
* Save and restart the NodeServer

* Polyglot Configuration

![Polyglot Configuration](https://github.com/sjpbailey/udi-poly-baspi-6u6r-python-master-v3/blob/0405c4b5853a0e7afb22bcc76450b732a73f0590/Archive-images/Polyglot-config.png)
