---
comments: true
title: Guides for SV06 (Plus)
description: Useful guides and tutorials for SV06 and SV06 Plus
---

## Bed Leveling Guide

<https://www.reddit.com/r/Sovol/comments/10xnu7k/sv06_perfect_first_layer_across_the_entire_build/>

## Bed Leveling Test

> A quick test for adjusting your Z-Probe Offset while printing with the SV06, it draws the skirt right next to the purge line, check this in your .gcode file with your slicer beforehand. You can adjust your Z-Probe Offset while printing until you get the desired results. Make sure to Autolevel your bed before doing a Bed Level Test.

[by @PleaseHelp on Printables](https://www.printables.com/model/376835)
[by @stormy on Printables](https://www.printables.com/model/445074/files)

## Inductive Sensor X Axis Tramming

Use the SV06's inductive sensor to tram the X-axis since the built-in method doesn't work for everyone. [Guide from r/Sovol](https://www.reddit.com/r/Sovol/comments/10z4nyx/sv06_inductive_sensor_x_axis_tramming/).

## Z-axis Bearing Removal

[Reddit post](https://www.reddit.com/r/Sovol/comments/129zwxa/sovol_sv06_z_axis_bearings_removal/?utm_source=share&utm_medium=web2x&context=3)

## LM8UU vs Igus RJ4JP (Drylin) Bearings

[Reddit post](https://www.reddit.com/r/Sovol/comments/128hf2a/lm8uu_vs_igus_rj4jp_drylin/?utm_source=share&utm_medium=web2x&context=3)

## Improving Part Cooling Stock Fan Performance

Source [Sovol forum](https://forum.sovol3d.com/t/sv06-overhangs-curling-upwards-making-nozzle-knock-over-the-print/1335/26?u=blakadder):

I think I found what causes the bad part cooling.

1. First of all, part cooling fan facing down is a terrible design decision. It sucks hot air from the heated bed, resulting in less efficient part cooling.
2. 4010 fan isn’t powerful enough.
3. Inefficient part cooling shroud which blows from the front and a bit from the left, providing less cooling to the back and to the right side of the print. Some other printers have more advanced shrouds which blow from the opposite sides (left/right).

But these reasons don’t explain why some users like @AdamByram get perfect benchy from SD card (185C/60C/100 fan) while other users like me suffer from undercooling even with 100% part cooling fan.

Here comes reason #4 - _**assembly issues**_.

Please take a look at the photo of a part cooling fan base plate:

![Screw location to improve part cooling](/images/troubleshooting/improvepartcooling.webp)

These hex screws allow some forward/back adjustment of the base plate. Looks like during extruder assembly it can be adjusted all the way forward, all the way back or somewhere in between.
I think this is the main reason of inconsistent cooling on different machines.
Users who suffer from undercooling with 100% part cooling fan should try to adjust the part cooling fan baseplate and see if it helps.

## Video Guides from Sovol

[Video Guides](videos.md)

## Install Octoprint on Windows

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/gwHarFUTGnA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## IKEA Lack Table Enclosure

[@RReuter_493554 on Printables](https://www.printables.com/model/347706)