# Jaguar Land Rover Node Server

![Land Rover ](<https://github.com/sjpbailey/Documentation/blob/def2b49d817b030fc50568c860b3b70b27d91154/Jaguar_LandRover/images/IMG_9194.jpg>)

* The purpose of this Nodeserver is for custom control of Jaguar, Land Rover, Range Rover Vehicles.

* Python 3.9

![Admin Console ](<https://github.com/sjpbailey/Documentation/blob/e12c57def5151f4182e4f43c8368fbb8b738f064/Jaguar_LandRover/images/IMG_9195.jpg>)
![Admin Console ](<https://github.com/sjpbailey/Documentation/blob/main/Jaguar_LandRover/images/landrover-parameters.png>)

## Configuration

### Defaults

* Default Short Poll:  Every 10 minutes
* Default Long Poll: Every 30 minutes (heartbeat)

#### User Provided

* Enter Your Access ID as apiAccessId = "Your Email"
* Enter your Access Secret as apiSecret = "Your Password"
* Enter your Pin Number = "Your Pin"
* Save and if not running restart the NodeServer

##### Python Module jlrpy

* This Node Server uses the jlrpy Python Module.

##### Documentation

The associated API documentation for the JLR InControl API is a good read for anyone wanting to make use of this project. It's currently available [here](https://documenter.getpostman.com/view/6250319/RznBMzqo)
