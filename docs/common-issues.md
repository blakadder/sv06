---
comments: true
title: Common Issues with SV06 (Plus)
description: Common issues and their solutions for Sovol SV06 and SV06 Plus printers
---
## SV06 Help Center

Many common issues are listed at the  [Official SV06 Help Center](https://sovol3d.com/blogs/news/help-center-sv06). Check here first

## No Bed Adhesion

Can be caused by many factors:

- PEI sheet is not clean enough: Clean it thoroughly with dish soap and warm water then dry immediately. Maintain a clean surface with isopropyl alcohol and lint free cloth.
- Z-offset too high: Z-offset is so high that the nozzle doesn't squish the melted plastic onto the print sheet which results in poor or no adhesion.
- Bed mesh issues: Make sure to upgrade to latest firmware and that the startup G-Code in your slicer contains `M420 S1` to use the saved bed mesh.
- Gantry not square:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/N5qbWdmn0VM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Hot End Not Level

The nozzle sits at an angle and is not parallel to the axes. This commonly happens to a bent heat break. Some printers will print fine with this issue but others will show symptoms of un-levelled bed, it all depends on the way it bends and the severity of the bend.

This is a known factory assembly issue but can also be caused from excessive mechanical stress when changing the nozzle or improperly tightened screws (two) mounting the hotend to the extruder. 

Fixed by replacing the hot end or just the heat break. You can try to straighten it but there's danger of breaking.

To avoid always hold the heat block firmly with wrench or plies while tightening the nozzle. Don't overtighten the mounting screws and screw them in little by little alternating between the two.

[Reddit post with the issue](https://www.reddit.com/r/Sovol/comments/10vi5j0/hot_end_not_level_is_this_normal_got_the_feeling/)

## Noisy Bearings

The gravelly sound when the bearings are travelling over the linear rods is caused by Sovol sending out dry, unlubricated bearings. 

Quick fix is [lubricating the rods](/first-steps/#lube-linear-rods). Best fix is packing them with grease as shown by [lost in tech](https://www.youtube.com/@foundintech) and [SavageLau](https://www.youtube.com/@SavageLau):

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/6-iKoJXXwnM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/lUvaA4fJWH0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Motor Mounts Not 90°

Motors aren't at a true 90° angle to the frame due to mounts. This occurs on Z-axis and Y-axis motor mounts. 

You can try to bend the bracket but that requires some disassembly. As a quick fix print [this shim](https://www.printables.com/model/360276) and mount it between the motor and the extrusion.

![Shim the motor mount](/images/troubleshooting/motor_not_true.webp)

## SV06 Plus Silicone Sock Doesn't Fit

From Facebook SV06 User Group:

> I, like a couple other SV06 Plus owners, got into an issue with a blobby mess leaving the printer unattended. Mine was quite bad and lots of filament got between the heat block and sock and ended up covering the delicate wiring for the thermistor. Sovol was kind enough to send me a replacement hot end which was greatly appreciated. What I noticed about the replacement is that part of the silicone sock is trimmed away making space for the wire for the heat cartridge. Prior to the revision, the wire was pushing down one corner of the sock causing it to fit poorly. I would have to constantly pull it up but during a print it would sag back down. Like wearing loose pants and pulling it up all the time. My guess is that the sock came down during my unattended print and once it caught a bit of melted filament it blobbed.
From my picture of the new vs old you can see they've trimmed the corner. My advice here is if you have one side of the sock sagging down, remove it and trim a tiny bit to make clearance for the cartridge wiring. Hopefully this saves you any potential issue that I experienced.

![Silicone Sock Issue](/images/plus/silicone_sock_difference.jpg)
