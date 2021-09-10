# esp-gate
Control an automatic gate using HomeKit with an esp8266 and homebridge. 

# Requirements 
- homebridge server
- homebridge-http-garage plugin (https://github.com/Tommrodrigues/homebridge-http-garage)
- esp8266 (D1 mini)
- Relay (D1 mini shield) 
- Contact sensor
- Static IP for esp8266
- Automatic gate
- Trigger pin on gate circut 

# Homebridge Server
The windows 10 version was used as a service. How to do this is here https://github.com/homebridge/homebridge/wiki/Install-Homebridge-on-Windows-10

# homebridge-http-garage
Install this plugin as seen here: https://github.com/Tommrodrigues/homebridge-http-garage#installation

The configuartion of this plugin I used that works with the esp8266 program is here:
```
{
            "accessory": "GarageDoorOpener",
            "name": "gate",
            "apiroute": "http://192.168.0.32",
            "openTime": "10",
            "closeTime": "7",
            "pollInterval": "1000"
}
```
The IP address is dependant on your situation. You should be able to obtain this through your router settings. More on this plugin can be found at the link in the requirements section.

# esp8266 D1 mini
Any esp8266 can be used but the D1 mini is really easy to work with and has many avalible shields. I also used the D1 mini relay sheild.
I purchased them both from here: https://www.aliexpress.com/item/4000420770002.html

# Contact Sensor
Any reed switch will work. Must be closed when gate is closed. Not required as code can be altered. 

# Static IP
 Set a static IP address for your esp8266. Differs from router to router so it will not be discussed in this guide. 
 
 # Gate
 Must have a trigger pin that is able to be triggered using a relay. 
 
 # Instructions
 1. Connect the contact sensor to ground and D1 of the esp8266.
 2. Connect the relay to D5 (or use the sheild)
 3. Download the code to the esp8266 from here: https://github.com/ixy05/esp-gate/ code will go here
 4. Adjust pins if you changed them and input your Wifi credentials. 
 5. Install the gate sensor, the sensor and the magenet together when the gate is closed. 
 6. Connect the trigger and ground of the gate cicut to the relay shield. 

# Schematic
image will go here
