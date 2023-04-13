---
comments: true
---
# Firmware

## Marlin 

### Sovol Firmware

Original Sovol firmware

[Download](https://sovol3d.com/pages/download){ .md-button }
[Source](https://github.com/Sovol3d/Sv06-Source-Code){ .md-button }

### hillsoftware's build

Custom Sovol SV06 build with options for UBL, Bi-Linear, Manual Mesh, Input Shaping, and X-Twist

[Download](https://github.com/hillsoftware/sv06/releases){ .md-button }
[Source](https://github.com/hillsoftware/sv06){ .md-button }

### blastrock's build

This is an attempt at cleaning up branches from various other firmwares while providing a working Marlin 2.1.2 firmware with X-Twist compensation support.

[Download](https://github.com/blastrock/Marlin-sv06/releases){ .md-button }

### TH3D Unified 2 Firmware

<https://support.th3dstudio.com/helpcenter/sovol-sv06-firmware/>

## Klipper

### One-Stop-Shop Sovol SV06 Klipper Configuration

A comprehensive [Klipper configuration](https://github.com/bassamanator/Sovol-SV06-firmware/) for multiple variants of the Sovol SV06.

##### Supports
 
- SV06
- SV06 Plus
- SV06 with the BTT SKR-Mini-E3-V3.0

### Pr20100+ Klipper profile

Complete Klipper profile with all config files and macros to tune the Sovol SV06 (stock).

<https://github.com/Pr20100/SOVOL-SV06-Klipper-profile>

### spinixguy's build

<https://github.com/spinixguy/Sovol-SV06-firmware>

### Enable Buzzer Macro

Want to use the beeper (M300) G-Code to alert you?

Add this to your macros in Klipper:

```sh
######################################################################
# Beeper
######################################################################
# M300 : Play tone. Beeper support, as commonly found on usual LCD
# displays (i.e. RepRapDiscount 2004 Smart Controller, RepRapDiscount
# 12864 Full Graphic). This defines a custom I/O pin and a custom
# GCODE macro.  Usage:
#   M300 [P<ms>] [S<Hz>]
#   P is the tone duration, S the tone frequency.
# The frequency won't be pitch perfect.
[output_pin BEEPER_pin]
pin: PC6
#   Beeper pin. This parameter must be provided.
#   ar37 is the default RAMPS/MKS pin.
pwm: True
#   A piezo beeper needs a PWM signal, a DC buzzer doesn't.
value: 0
#   Silent at power on, set to 1 if active low.
shutdown_value: 0
#   Disable at emergency shutdown (no PWM would be available anyway).
cycle_time: 0.001
#   Default PWM frequency : 0.001 = 1ms will give a tone of 1kHz
#   Although not pitch perfect.
[gcode_macro M300]
gcode:
    # Use a default 1kHz tone if S is omitted.
    {% set S = params.S|default(1000)|int %}
    # Use a 10ms duration is P is omitted.
    {% set P = params.P|default(100)|int %}
    SET_PIN PIN=BEEPER_pin VALUE=0.5 CYCLE_TIME={ 1.0/S if S > 0 else 1 }
    G4 P{P}
    SET_PIN PIN=BEEPER_pin VALUE=0
```

Borrowed from: https://dev.to/wallclocks/enable-buzzer-in-klipper-for-creality-boards-422-427-19mg
