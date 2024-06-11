---
layout: default
title: Basics
nav_order: 2
parent: Initial setup
---

## Basic requirements

You can use TemperBridge with or without Home Assistant. Regardless, you will need:

- A supported model of adjustable base - I cannot stress this enough, [please make sure your remote control matches the one depicted here]({{ "/" | relative_url }}).
- WiFi network
- PC, phone, or tablet for initial setup
- Home Assistant version **2023.2** or later (if using with Home Assistant, of course)
- USB A power supply - measured power consumption is around 2-3 W. An old phone charger or spare USB port on a PC should work just fine.
- The info page that came with your TemperBridge which gives the MAC address and device passwords.

## Determine the remote control channel number

The first step is to figure out which channel your remote control uses. To do this, simply
hold the **Stop** + **Flat** buttons for 10 seconds. The channel number will appear on the screen for 10 seconds.

{: .warning }
After the channel number appears on the screen, don't press any buttons until it disappears (after about 10 seconds).
Otherwise, you may inadvertently change the channel number to which your remote is tuned. If that happens, you'll need to go
through one of the learning procedures detailed [in the manual](https://assets-www.tempurpedic.com/media/documents/Tempur_Ergo_Premier_Owners_Manual.pdf){:target="_blank"}.

If you have a split base that is _not_ operating in tandem mode, then each remote will have its own channel.

## Next steps

Next, you'll need to [connect your TemperBridge to your WiFi network]({{ "/docs/initial_setup/connect_to_wifi" | relative_url }}).