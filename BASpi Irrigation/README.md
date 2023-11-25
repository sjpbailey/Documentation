# Universal Devices WiFi Irrigation NodeServer

## Based on the Contemporary Controls BASpi and the BASpi-Edge SYS6U6R BACnet/IP WiFi/IP Control Devices

* This controllers can be used to control low voltage switchable devices for any advanced control sequence attached via ethernet or Wi-Fi IP.

## Reason

* The purpose of this Nodeserver is for custom control through the ISY for Irrigation and general Home automation for multiple control operations, WiFi, IP, BACnet.

* It utilizes Contemporary Controls BASpi-6U6R and the BASpi-Edge-6U6R BACnet control Modules for up to six (6) irrigation zones totalling 36 Zones.
Please see links below for information & configuration of this Device within Contemporary Controls GUI.

* Each BASpi Controller with its six zone outputs also has six universal inputs with the first input configured for outside air temperature in degrees fahrenheit and the last input configured for moisture or volumetric water content sensor in percent using a 0-10vdc volumetric transmitter. Finally with inputs 2-4 for raw value UOM's for your choice in configuration. Six Zones per Node installed by the controller based on your user key and value, for key nodes you enter up to 6. For each BASpi device you will need to add an IP Address. For the IP address you will enter for your key, irrip_0 - irrip_6. Then for value, the BASpi IP Address. The final image shows an example of my home using two BASpi Controllers, so for nodes i have a value of 2, and for each BASpi I have ones as key irrip_0 value 192.168.1.15 and the second BASpi controller input as key irrip_1 value 192.168.1.15.
  
* It is Best to use the Open Weather Map/WeatherBit Nodeserver to bring in your local weather conditions into your ISY to lock out your irrigation, if humidity, temperature, or even wind conditions make it unnessessary to water your landscaping! <https://github.com/bpaauwe/udi-owm-poly>

* This Network BAS series will include in the near future custom home control for Garage Door, Pool Control, Well Pump Control, HVAC, VVT, Boiler, along with any custom control you create utilizing the pip bascontrolns module <https://pypi.org/project/bascontrolns/>.

* This controller sits on a Raspberry Pi. You can easily add it to your ISY after you configure its ip address also add a camera to it.

* Irrigation Zone Control Wiring

![CAD Wiring](https://github.com/sjpbailey/Documentation/blob/main/BASpi%20Irrigation/Archive%20Images/CAD-Irrigation.png)

* Irrigation Zone Control ISY Node

![Irrigation Zone Node](https://github.com/sjpbailey/Documentation/blob/main/BASpi%20Irrigation/Archive%20Images/Zone-Node.png)

* Irrigation Zone Controller ISY Program

![Program](https://github.com/sjpbailey/Documentation/blob/main/BASpi%20Irrigation/Archive%20Images/program1.png)

* Irrigation Zone Controller Alarm and ShutDown ISY Program

![Program](https://github.com/sjpbailey/Documentation/blob/main/BASpi%20Irrigation/Archive%20Images/Alarm%20and%20shutdown1.png)

* Example program to cycle six zones On Alexa <https://youtu.be/htW2vVqgODw>

### BASpi-SYS6U6R and the BASpi-Edge DIY BacNet Control Device by Contemporary Controls

* Main
[Contemporary Controls BASpi DIY](https://www.ccontrols.com/basautomation/baspi.htm)
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
* BASpi Controller Configuration
[Contemporary Controls BASpi Configuration Quick Start](https://www.ccontrols.com/pdf/is/BASPI-QSGuide.pdf)

#### Future

* You can add up to six (6) BASpi Device controllers
  
![Input Config](Documentation/blob/main/BASpi%20Irrigation/Archive%20Images/shot_3.png)

[Universal Input Configuration Video](https://www.youtube.com/watch?v=hTd1mR7npP4)

* Python 3.7.7

##### Configuration

###### Defaults

* Default Short Poll:  Every 2 minutes
* Default Long Poll: Every 4 minutes (heartbeat)

###### Requirments

* requests
* bascontrolns >= 0.0.3
* udi_interface

###### User Provided

* Enter the number of Baspi nodes you desire 0-5 Key = nodes Value = 0-5
* Enter your IP address for up to six (6) BASpi-SYS6U6R controller,
* Config: key = irrip_* (* = 0-5) Value = Enter Your BASpi IP Address, Example: key irrip_0  value 192.168.1.50
* Save and restart the NodeServer

* Irrigation Polyglot Configuration

![BAS Irrigation Polyglot Configuration](https://github.com/sjpbailey/Documentation/blob/main/BASpi%20Irrigation/Archive%20Images/configuration.png)
