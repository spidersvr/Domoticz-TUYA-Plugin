# Domoticz-TUYA-Plugin
TUYA Plugin for Domoticz home automation

Controls TUYA devices your network (on/off switches and TUYA Lights)

## Key Features

* Auto-detects devices on your account
* Tested with lights and switches (but should control other devices on/off)
* Cloud control only uses your user/password account with encrypted communications without requiring IP or device IDs or Keys to configure it

## Installation

Python version 3.4 or higher required & Domoticz version 3.9446 or greater.

To install:
* Go in your Domoticz directory using a command line and open the plugins directory.
* Run: ```git clone https://github.com/guino/tuyaha.git```
* Restart Domoticz.

## Updating

To update:
* Go in your Domoticz directory using a command line and open the plugins directory then the Domoticz-TUYA directory.
* Run: ```git pull```
* Restart Domoticz.

## Alternate Install/Update:

* Simply create a directory under domoticz/plugins directory like 'TUYA' and download/copy the plugin.py file and tuyaha directory (with all its contents) into it.
* Restart Domoticz.

## Configuration

Enter your username and password for your tuya account along with your country code (1=US/Canada, 55=Brazil, etc). The initial setup of your devices should be done with the TUYA app and this plugin will detect/use the same settings and automatically find/add the devices into Domoticz.

## Usage

In the web UI, navigate to the Hardware page. In the hardware dropdown there will be an entry called "TUYA" -- configure and add the hardware there.
Devices detected are created in the 'Devices' tab, to use them you need to click the green arrow icon and 'Add' them to Domoticz.

## Change log

| Version | Information|
| ----- | ---------- |
| 1.0.0 | Initial upload version |

# Includes 'tuyaha' project:

Cloned from the abandoned package [tuyapy](https://pypi.org/project/tuyapy/) v0.1.3. This package implements a Tuya
API endpoint that was specially designed for Home Assistant.

This clone contains several critical fixes. Check commits.

## How to check whether the API this library using can control your device?

- Copy [this script](https://github.com/PaulAnnekov/tuyaha/blob/master/tools/debug_discovery.py) to your PC with Python
  installed or to https://repl.it/
- Set/update config inside and run it
- Check if your devices are listed
  - If they are - open an issue and provide the output
  - If they are not - don't open an issue. Ask [Tuya support](mailto:support@tuya.com) to support your device in their 
    `/homeassistant` API
- Remove the updated script, so your credentials won't leak
