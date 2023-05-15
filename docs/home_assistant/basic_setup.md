---
layout: default
title: Basic setup
nav_order: 2
parent: Home Assistant
---

## Home Assistant entities

As a starting point, here is code for an 'Entities' card that has the most useful entities exposed:

```yaml
type: entities
entities:
  - entity: number.bedroom1_channel
  - entity: button.bedroom1_flat
    secondary_info: none
  - entity: button.bedroom1_preset_1
  - entity: button.bedroom1_preset_2
  - entity: button.bedroom1_preset_3
  - entity: button.bedroom1_preset_4
  - entity: button.bedroom1_stop
  - entity: button.bedroom1_massage_mode_1
  - entity: button.bedroom1_massage_mode_2
  - entity: button.bedroom1_massage_mode_3
  - entity: button.bedroom1_massage_mode_4
  - entity: number.bedroom1_head_massage_intensity
  - entity: number.bedroom1_lumbar_massage_intensity
  - entity: number.bedroom1_leg_massage_intensity
  - entity: light.bedroom1_green_led
    secondary_info: brightness
  - entity: button.bedroom1_head_up
  - entity: button.bedroom1_head_down
  - entity: button.bedroom1_legs_up
  - entity: button.bedroom1_legs_down
title: Bedroom
```