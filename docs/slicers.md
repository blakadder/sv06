# Slicer Configurations

## Cura

SV06 printer profile is included in Cura v5.3+

### Material Profiles

- [PETG](/files/PETG.curaprofile)
- [PETG for 0.6 nozzle](/files/jeremy_petg_06_super_fast.curaprofile)
- [TPU](/files/TPU.curaprofile)
- [TPU for 0.6 nozzle](/files/TPU_06.curaprofile)

### Improved Startup G-Code

??? info "G-Code"
    ```gcode
    G92 E0 ; Reset Extruder
    G28 ; Home all axes
    G92 E0 ; Reset Extruder
    G1 Z3.0 F3000 ; Move Z Axis Up
    G1 X3.0 Y200.0 F5000 ; Move to Start Line

    M104 S165 ; Set Hotend Tempurature
    M140 S{material_bed_temperature_layer_0} ; Set Bed Temp
    M190 S{material_bed_temperature_layer_0} ; Wait for Bed Temp

    G1 Z1.0 F150 ; Lower Nozzle
    M104 S{material_print_temperature_layer_0} ;Set Hotend Temp
    M109 S{material_print_temperature_layer_0} ;Wait for Hotend Temp
    G1 Z0.28 F150 ; Ready to Purge

    G4 S2 ; Dwell
    G1 X3.0 Y3.0 Z0.28 F1500 E15 ; Draw First Line
    G1 X3.0 Y3.3 F5000
    G1 X50.0 Y3.3 Z0.28 F1500 E30 ; Draw Second Line
    G92 E0 ; Reset Extruder
    G1 Z 3.0 F3000 ; Move Z up to prevent Scratching
    ```

### SV06 Plus Profile

[https://www.reddit.com/r/Sovol/comments/12ycn1g/tip_this_is_how_you_can_import_sovol_slicers_sv06/](https://www.reddit.com/r/Sovol/comments/12ycn1g/tip_this_is_how_you_can_import_sovol_slicers_sv06/)

## PrusaSlicer

### Ehmc130's PrusaSlicer Profile

Source [Ehmc130's post on /r/Sovol](https://www.reddit.com/r/Sovol/comments/11ov0pv/sovol_sv06_prusa_slicer_profile_recommendations/):

PRUSA SLICER PROFILE: My profile for Prusa Slicer is based on the Prusa i3 MK3S+ profile and for good reason. The SV-06 is basically a clone under a different name which is why Prusa Slicer lends itself well for the SV-06. I’ve adjusted print volume, retraction, some end Gcode, and a few other minor things so you don’t have to.

Begin by downloading PrusaSlicer [here](https://www.prusa3d.com/page/prusaslicer_424/).

Run through the installer as you normally would.

When you open PrusaSlicer for the first time the Configuration Wizard should come up. From there click Prusa FFF → Under MK3 Family put a checkmark on the .4mm nozzle under Original Prusa i3 MK3S & MK3S+ → Click Finish at the bottom and close PrusaSlicer. (The reason we added the MK3S and S+ is so we can use the print settings presets in PrusaSlicer.)

Download my SV06 printer profile & filament presets [here](https://www.dropbox.com/s/ac28w7qjaiq0rf7/Sovol%20SV-06%20Prusa%20Slicer%20Config.rar?dl=0) (updated as of 4/8/23) and unpack it.

This folder includes a printer folder and a filament folder → Add the config files I’ve provided to their corresponding folders (refer to the next step) and that’s it → You now have your printing settings from the MK3S profile, your print profile from my config, and the filament presets I’ve found to be reliable.

Click Help in PrusaSlicer → Show Configuration Folder

_(Windows)_ Open Windows Explorer → Click the view tab at the top → Make sure the box Hidden Items is checked → Navigate to the following folder: C:\Users\Your User Profile\AppData\Roaming\PrusaSlicer.

_(Mac)_ Open Finder → Navigate to the following folder: /Users/<user\>/Library/Application Support/PrusaSlicer

### Darren's Config Bundle

Has both SV06 and SV06 Plus and an 0.6 nozzle version of both printers as well. It has profiles for different layer heights/quality.

[Download](/files/PrusaSlicer_config_bundle.ini){ .md-button .md-button--primary }

### Chris' Profile Pack

Adds the ability to select all Sovol printers in the PrusaSlicer Configuration Wizard.

Just extract and drop it into your Prusaslicer location, f.e "C:\Program Files\Prusa3D\PrusaSlicer\resources\profiles"

[Download](/files/prusaslicer_profiles_chris.zip){ .md-button .md-button--primary }

### Preston's SV06 Plus Profile

[Download](/files/Preston_SV06Plus_Prusaslicer.ini){ .md-button .md-button--primary }

## OrcaSlicer 

SoftFever/OrcaSlicer configuration with nozzle 0.4 base Marlin profile and a 0.6 Klipper profile.

[Download](/files/SoftFever.rar){ .md-button .md-button--primary }

