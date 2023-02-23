---
layout: default
title: Initial setup
has_children: true
nav_order: 2
---

## Basic requirements

You can use TemperBridge with or without Home Assistant. Regardless, you will need:

- A supported model of adjustable base - I cannot stress this enough, [please make sure your remote control matches the one depicted here]({{ "/" | relative_url }}).
- WiFi network
- PC, phone, or tablet for initial setup
- USB A power supply - measured power consumption is around 2-3 W. An old phone charger or spare USB port on a PC should work just fine.
- The info page that came with your TemperBridge which gives the MAC address and device passwords.

## Determine the remote control channel number

The first step is to figure out which channel your remote control uses. To do this, simply 
hold the **Stop** + **Flat** buttons for 10 seconds. The channel number will appear on the screen for 10 seconds.

{: .warning }
After the channel number appears on the screen, don't press any buttons until it disappears (after about 10 seconds). 
Otherwise, you may inadvertently change the channel number to which your remote is tuned. If that happens, you'll need to go 
through one of the learning procedures detailed [in the manual](https://assets-www.tempurpedic.com/media/documents/Tempur_Ergo_Premier_Owners_Manual.pdf).

If you have a split base that is _not_ operating in tandem mode, then each remote will have its own channel. 

## Connect to your WiFi network

Power up the TemperBridge. After a few moments, the red LED will blink. Using your PC or phone, connect to the
**TemperBridge Wifi Config** WiFi network. This is a special WiFi network (called a [captive portal](https://esphome.io/components/captive_portal.html)) that the TemperBridge creates
when it is not otherwise connected to WiFi. 

Upon connecting, your browser should automatically open the captive portal web interface. (If not, go to [http://192.168.4.1/](http://192.168.4.1/)).

<img width="500px" src="{{ "/assets/images/captive-portal.PNG" | relative_url }}">

Click your WiFi network, enter the password, then click Save. After about 30 seconds, the **TemperBridge Wifi Config** network will disappear. 
Your TemeprBridge should now be connected to WiFi.

## Verifying connectivity 

The hostname of your TemperBridge will be something like **temperbridge-3f65e1**. The last six characters are the same as the last
three octets of the MAC address. You can find both the MAC address and hostname on the info page that came with your device.

TemperBridge uses [mDNS](https://en.wikipedia.org/wiki/Multicast_DNS) to advertise itself on your network which is how Home Assistant finds it.

Try pinging your device's hostname with **.local** tacked onto the end. For example: 

```bash
ping temperbridge-3f65e1.local
```

If this fails, check to make sure your system has mDNS support enabled. On Windows, the easiest fix is to 
install [Bonjour Print Services](https://support.apple.com/kb/DL999?locale=en_US) and then reboot your machine. On Linux, try following [these instructions](https://developer.ridgerun.com/wiki/index.php/How_to_use_mDNS_to_access_a_device_without_knowing_the_IP_address).

## Usage with Home Assistant 
You will almost certainly want to use TemperBridge as part of a [Home Assistant](https://www.home-assistant.io/) 
installation. Therefore, you will need to have installed and configured Home Assistant. For instructions, see: https://www.home-assistant.io/installation/.

Next, you will need to 