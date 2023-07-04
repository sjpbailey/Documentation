# Universal Devices Tuya Product NodeServer

* ![Tuya Sweeper](<https://github.com/sjpbailey/Documentation/blob/eae2457d3c3c6016d8a92fd06dfb4bcad3790ba4/Tuya%20Robot%20Sweeper/images_go/RobotPic.png>)

## Currently for Tuya Smart Life Robot Sweeper Vacuum


![Tuya Robot Sweeper ](<https://github.com/sjpbailey/Documentation/blob/eb79ac7e3b3bdfe9227e1599c1442cbdfbc881a9/Tuya%20Robot%20Sweeper/images_go/Sweeper_1.png>)

* Device Model Numbers:
* Smart Life - G20 Sweeper Vacuum

* This pulls Device Data from your configured Tuya API Account
* You must first create a Tuya Account and have your Devices functional on the Tuya Smart Phone App.

1. TUYA ACCOUNT - Set up a Tuya Account
2. Please watch quick video [From This Smart House](https://youtu.be/M9Q6de08QOI)

* Create a Tuya Developer account on [iot.tuya.com](https://iot.tuya.com/).
* [Tuya](https://en.tuya.com/) devices are designed to communicate with the TuyaCloud, allowing us to directly control the devices using the cloud. This python connector module authenticates your devices.
* [Tuya Instructions](https://developer.tuya.com/en/docs/iot/quick-start1?id=K95ztz9u9t89n)
* [PDF Instructions](<https://github.com/sjpbailey/Documentation/blob/376539c10801b161a066426a90f09d0a2026b84c/Tuya%20Robot%20Sweeper/images_go/Tuya.IoT.API.Setup%20(3).pdf>)
* Click on "Cloud" icon -> "Create Cloud Project"
* 1. Remember the "Data Center" you select.([screenshot](https://github.com/sjpbailey/Documentation/blob/376539c10801b161a066426a90f09d0a2026b84c/Tuya%20Robot%20Sweeper/images_go/Screenshot%202023-06-18%20at%2011.10.44%20PM.png)).
* 2. Skip the configuration wizard but remember the Authorization Key: *API ID* and *Secret* for below ([screenshot](https://github.com/sjpbailey/Documentation/blob/376539c10801b161a066426a90f09d0a2026b84c/Tuya%20Robot%20Sweeper/images_go/Screenshot%202023-06-18%20at%2011.11.41%20PM.png)).
* Click on "Cloud" icon -> Select your project -> **Devices** -> **Link Tuya App Account** ([see screenshot](https://user-images.githubusercontent.com/836718/155827671-44d5fce4-0119-4d0e-a224-ef3715fafc24.png))
* Click **Add App Account** ([screenshot](https://user-images.githubusercontent.com/836718/155827671-44d5fce4-0119-4d0e-a224-ef3715fafc24.png)) and it will display a QR code. Scan the QR code with the *Tuya Smart app* on your Phone (see step 1 above) by going to the "Me" tab in the *Tuya Smart app* and clicking on the QR code button `[..]` in the upper right hand corner of the app. When you scan the QR code, it will link all of the devices registered in your *Tuya Smart app* into your Tuya IoT project.
* **NO DEVICES?** If no devices show up after scanning the QR code, you will need to select a different data center and edit your project (or create a new one) until you see your paired devices from the *Smart Life App* show up. ([screenshot](https://github.com/sjpbailey/Documentation/blob/376539c10801b161a066426a90f09d0a2026b84c/Tuya%20Robot%20Sweeper/images_go/Screenshot%202023-06-18%20at%2011.13.45%20PM.png)). The data center may not be the most logical. As an example, some in the UK have reported needing to select "Central Europe" instead of "Western Europe".

* **SERVICE API:** Under "Service API" ensure these APIs are listed: `IoT Core`, `Authorization` and `Smart Home Scene Linkage`. To be sure, click subscribe again on every service.  Very important: **disable popup blockers** otherwise subscribing won't work without providing any indication of a failure. Make sure you authorize your Project to use those APIs:
* Click "Service API" tab
* Click "**Go to Authorize**" button
* Select the API Groups from the dropdown and click `Subscribe` [screenshot](<https://github.com/sjpbailey/Documentation/blob/376539c10801b161a066426a90f09d0a2026b84c/Tuya%20Robot%20Sweeper/images_go/Screenshot%202023-06-18%20at%2011.14.31%20PM.png>)

## Requirements-

1. udi-interface
2. tuya-connector-python
3. tinytuya 1.12.7

### Release Notes

* Enter Your Access ID as apiAccessId = "Your API Access ID
* Enter your Access Secret as apiSecret = Your API Secret

* ![API ACCESS ID and SECRET Location](https://github.com/sjpbailey/Documentation/blob/376539c10801b161a066426a90f09d0a2026b84c/Tuya%20Robot%20Sweeper/images_go/Screenshot%202023-06-16%20at%203.57.31%20PM.png)

* API UID as apiUid = Your UID found Tuya Site key = baspi_ip Value = Your IP Address.

* ![UID Location](<https://github.com/sjpbailey/Documentation/blob/376539c10801b161a066426a90f09d0a2026b84c/Tuya%20Robot%20Sweeper/images_go/Screenshot%202023-06-16%20at%203.51.36%20PM.png>)

* API Endpoint as apiEndpoint = https:// openapi.tuyaus.com/
* API MQ Endpoint as apiMq = wss://mqe.tuyaus.com:8285/
* *Region* (cn, us, us-e, eu, eu-w, or in) So the (tuyaus) in the links above = us = USA, cn = Canada etc...

* 3.0.1 06/16/2023

* Initial version published to github
