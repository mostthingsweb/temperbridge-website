---
layout: default
title: Home Assistant
has_children: true
nav_order: 3
---

## Version requirement

TemperBridge is supported on Home Assistant version **2023.2** and later. Please update HA to at least 2023.2 before purchasing and setup.

It *may* work on earlier versions but I cannot guarantee it. Also, regardless of what version of HA you are using,
the ESPHome integration version needs to be at least [2021.9.0](https://esphome.io/changelog/2021.9.0.html) since that's
when support for encryption keys was added.

## Device setup

Please complete [Initial Setup]({{ "/docs/initial_setup" | relative_url }}) before proceeding. This section assumes your TemperBridge is powered up and connected to your WiFi network.

**NOTE**: If you followed "Method 1" of WiFi setup, you may have already performed the steps in this section.

If using a version of Home Assistant before 2023.2, you will need to install the [ESPHome integration](https://www.home-assistant.io/integrations/esphome/).

Home Assistant should discover your TemperBridge automatically. It will give a notification that looks like this:

<img height="200px" src="{{ "/assets/images/notifications.PNG" | relative_url }}">

If after 5 minutes Home Assistant has not discovered your TemperBridge, try restarting Home Assistant.

Click "Check it out", then click the "Configure" button on the detected TemperBridge:

<img height="200px" src="{{ "/assets/images/discovered.PNG" | relative_url }}">

Click "Submit" on the popup:

<img height="200px" src="{{ "/assets/images/popup.PNG" | relative_url }}">

Enter the encryption key from the info page that came with your TemperBridge, then click "Submit". (If you have lost the info page,
please [contact us](https://www.temperbridge.com/contact) and we can send it to you.)

<img height="200px" src="{{ "/assets/images/encryption.PNG" | relative_url }}">

Finally, assign the TemperBridge to an area of your choice, and hit "Finish":

<img height="175px" src="{{ "/assets/images/area.PNG" | relative_url }}">
