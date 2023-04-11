---
comments: true
---

# First Steps

When you receive your SV06 (Plus) and assemble it per instructions do these steps first to avoid most common pitfalls.

## Lube linear rods

Sovol sends out printers with unlubricated bearings which sounds like walking on sand or gravel. As an emergency fix you can lube the rods with any kind of PTFE grease, lithium grease, skateboard lube or even fine machine oil. 

Wipe the rails clean of dirt and grime. Lightly lubricate the rod then run the bearing over them a couple of times. Repeat as necessary until the part moves silently and smoothly.

Recommended lubricants:

- WD40 Dry Lube with PTFE ([Amazon US](https://www.amazon.com/WD-40-300052-Specialist-Resistant-Spray/dp/B00AF0ODGM?keywords=wd40+dry+lube&qid=1681168661&sr=8-3&linkCode=ll1&tag=blakadders-20&linkId=d5ddcf4639dad80e4e807f181ab30243&language=en_US&ref_=as_li_ss_tl), [Amazon DE](https://www.amazon.de/-/en/WD-40-Specialist-Lubricant-49394-25NBA/dp/B098K1TGSC?crid=15HMWLGJEPKW1&keywords=wd40%2Bptfe&qid=1681168828&sprefix=wd40%2Bptfe%2Caps%2C101&sr=8-3&th=1&linkCode=ll1&tag=blakadders-20&linkId=3b900c7445c69ecc902a0f9dd3c0bb16&language=en_GB&ref_=as_li_ss_tl), [3D Jake](https://www.awin1.com/cread.php?awinmid=21809&awinaffid=930253&ued=https%3A%2F%2Fwww.3djake.com%2Fwd40%2Fspecialist-ptfe-dry-lubricant-spray))
- WD40 Dry Lithium Grease ([Amazon US](https://www.amazon.com/WD-40-Specialist-Protective-Lithium-Grease-Straw-Sprays/dp/B00L4QZ1VC?th=1&linkCode=ll1&tag=blakadders-20&linkId=15c680b23fb9dcc06ca78f78733c4200&language=en_US&ref_=as_li_ss_tl), [Amazon DE](https://www.amazon.de/-/en/WD-40-Specialist-White-Lithium-Grease/dp/B0913C2JLX?keywords=wd40%2Bweisses%2Blithium%2Bfett&qid=1681168799&sprefix=wd40%2Bwhite%2Blithi%2Caps%2C98&sr=8-4&th=1&linkCode=ll1&tag=blakadders-20&linkId=d8243e6724885decd1040765698018d0&language=en_GB&ref_=as_li_ss_tl))
- SuperLube lubricants ([Amazon US](https://www.amazon.com/s?k=Super+Lube&linkCode=ll2&tag=blakadders-20&linkId=8b1fd890fffb395066f04a8b3868317e&language=en_US&ref_=as_li_ss_tl), [Amazon DE](https://www.amazon.de/s?k=Super+Lube&linkCode=ll2&tag=blakadders-20&linkId=a88b9dd863f0ae93da72089be728d0a7&language=en_GB&ref_=as_li_ss_tl))

Take note that using wet lubricants will gather dust on the rods with time while dry lubricants will not but they need to be reapplied more often.

As a permanent fix you will need to disassemble the printer and pack the bearings with grease. [More info...](/troubleshooting/#dry-noisy-bearings)

## Tighten all screws

Hand tighten all visible screws.

Check the grub screw (set screw) inside the extruder. Completely unscrew the extruder tensioner screw and drop down the extruder lever. Rotate the extruder knob until you can see the grub screw inside. Tighten it as much as you can. Optionally: add a drop of thread locker or clear nail polish to secure it. Might affect future maintenance.

## Tighten the nozzle

Heat up the nozzle to high temperature, 250°C or more and hand tighten the nozzle with the supplied L wrench. Do not overtighten, that can damage the nozzle or bend your hotend.

## Tighten the belts

Use the belt tensioners to tighten the belts until they're not slack. There's no need to make them super tight like a guitar string, just enough that there's no chance of play or skipping over the pulley teeth. Take care not to overtighten the X-axis belt, that puts strain on the vertical linear rods and can warp them.

## Make sure the heated bed cable is not inside the gantry

The printer come with the the bed cable tucked below the bed. It is necessary to take it out so the bed can move freely from front to back in order for it to home correctly.

## Adjust Sensorless Homing

If your X and Y axis motors make terrible sounds during homing or completely stall you need to adjust sensorless homing in the firmware.

Navigate to *Configuration --> Advanced Settings --> TCM Drivers --> Sensorless Homing* and raise the value for the axis that needs it. Common recommendation is between 68 and 75 or even higher. You need the axis to hit the gantry with only a tap instead of ramming into it. Save configuration after you're done.

## Print these immediately

- [Heated bed cable guide](https://www.printables.com/model/409689-heatbed-cable-support-for-sovol-sv06-3d-printer): mandatory, will keep your cable from rubbing against the printer and snagging
- [Cable strain relief](https://www.printables.com/model/423797-cable-strain-relief-for-sovol-sv06-curve): I prefer this version since it works great in combination with the cable guide
    - [Smaller angle version](https://www.printables.com/model/432542-sovol-sv06-strain-relief)
    - [Short version](https://www.printables.com/model/409689-heatbed-cable-support-for-sovol-sv06-3d-printer)
- [Belt Mounted Y-Stop](https://www.printables.com/model/410274-gt2-belt-mounted-y-stop-for-sovol-sv06-3d-printer)

Make sure to like all the models and post your prints!

### and these if you want to

- [Print Head Cable Support](https://www.printables.com/model/427286-sovol-sv06-plus-print-head-cable-support): helps to keep the print head cable above the prints
- [Snap-on Screen Back Cover](https://www.printables.com/model/409672-lcd-display-back-cover-for-sovol-sv06-3d-printer): very easy to install back cover

## Get a better slicer

Download and install a better slicer and ditch Sovol's outdated fork of Cura.

[Ultimaker Cura](https://ultimaker.com/software/ultimaker-cura) comes with built in printer configuration for SV06.

[PrusaSlicer](https://www.prusa3d.com/page/prusaslicer_424/) can work with the MK3S configuration, just make the print surface 220x220x250 or use [SavageLau's configuration](https://www.printables.com/model/360315-printer-config).

## Learn to correctly load filament

This is how I always load filament. Preheat the nozzle for your material. Insert a cleanly cut filament end into the opening then use only the extruder wheel to load the filament half way. All the way until you hear a pop or the filament starts extruding is also fine. Then let the firmware continue with the purge.

Same method is recommended by [Sovol](https://www.youtube.com/watch?v=Y5XJXrT-9Ic).