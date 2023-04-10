# Enable Buzzer Sound

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