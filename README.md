# homebridge-mqttwindowblind
An homebridge plugin that create an HomeKit Window Blind Opener accessory mapped on MQTT topics

# Installation
Follow the instruction in [homebridge](https://www.npmjs.com/package/homebridge) for the homebridge server installation.
The plugin must be cloned locally (git clone https://github.com/iomax/homebridge-mqttwindowblind.git ) and should be installed "globally" by typing:

    npm install -g ./homebridge-mqttwindowblind
  
# Release notes
*** PAY ATTENTION : DON'T USE IT YET *** 
Version 0.0.0
+ Initial draft

# Configuration
Remember to configure the plugin in config.json in your home directory inside the .homebridge directory. Configuration parameters:
```javascript
{
  "accessory": "mqttwindowblind",
  "name": "SWITCH NAME",
  "url": "URL OF THE BROKER",
  "username": "USERNAME OF THE BROKER",
  "password": "PASSWORD OF THE BROKER",
  "caption": "SWITCH LABEL",
  "topics": {
		"openSet":        "MQTT TOPIC FOR THE SETTING OF THE OPEN STATUS",
		"closeSet":       "MQTT TOPIC FOR THE SETTING OF THE CLOSE STATUS",
		"openSetValue":   "OPTIONAL openSet PAYLOAD (DEFAULT true)",
		"closeSetValue":  "OPTIONAL closeSet PAYLOAD (DEFAULT true)",
		"openGet":        "OPTIONAL MQTT TOPIC FOR THE GETTING THE STATUS OF CLOSED SWITCH",
		"closedGet":      "OPTIONAL MQTT TOPIC FOR THE GETTING THE STATUS OF CLOSED SWITCH",
		"openGetValue":   "OPTIONAL VALUE THAT MEANS OPEN (DEFAULT true)",
		"closedGetValue": "OPTIONAL VALUE THAT MEANS CLOSED (DEFAULT true)",
            }
  "RunInSeconds": "OPEN/CLOSE RUN TIME IN SECONDS",
}
```

# Credit

The original homebridge MQTT plugins work was done by [ilcato](https://github.com/ilcato) in his [homebridge-mqttswitch](https://github.com/ilcato/homebridge-mqttswitch) project.


