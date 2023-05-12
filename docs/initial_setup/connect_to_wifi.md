---
layout: default
title: Connect to WiFi
nav_order: 2
parent: Initial setup
---


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
