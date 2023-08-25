# Jaguar Land Rover Node Server Custom Parameters

![Land Rover ](<https://github.com/sjpbailey/udi-poly-jaguar-landrover-v3/blob/e83be002bea14507fdb6a1b8e8ef0a4238bab394/images/IMG_9194.jpg>)

* The purpose of this Nodeserver is for custom control of Jaguar, Land Rover, Range Rover Vehicles.

* Python 3.9

![Admin Console ](<https://github.com/sjpbailey/udi-poly-jaguar-landrover-v3/blob/17cbfedbd3d53bc7d8987e24b3678cd19c415ec6/images/Screenshot%202023-08-19%20at%2010.07.40%20AM.png>)

## Configuration

### Defaults

* Default Short Poll:  Every 600 seconds
* Default Long Poll: Ever 10 minutes (heartbeat)

#### User Provided

* Enter Your Access ID as apiAccessId = "Your Email"
* Enter your Access Secret as apiSecret = "Your Password"
* Enter your Pin Number = "Your Pin"
* Save and if not running restart the NodeServer

##### Python Module jlrpy

* This Node Server uses the jlrpy Python Module.

##### Documentation

The associated API documentation for the JLR InControl API is a good read for anyone wanting to make use of this project. It's currently available [here](https://documenter.getpostman.com/view/6250319/RznBMzqo)
