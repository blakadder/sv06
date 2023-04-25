# Common Issues

## No bed adhesion

Can be caused by many factors:

- PEI sheet is not clean enough: Clean it thoroughly with dish soap and warm water then dry immediately. Maintain a clean surface with isopropyl alcohol and lint free cloth.
- Z-offset too high: Z-offset is so high that the nozzle doesn't squish the melted plastic onto the print sheet which results in poor or no adhesion.
- Bed mesh issues: Make sure to upgrade to latest firmware and that the startup G-Code in your slicer contains `M420 S1` to use the saved bed mesh.
- Gantry not square:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/N5qbWdmn0VM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Hotend not level

The nozzle sits at an angle and is not parallel to the axes. This commonly happens to a bent heatbreak. Some printers will print fine with this issue but others will show symptoms of un-levelled bed, it all depends on the way it bends and the severity of the bend.

This is a known factory assembly issue but can also be caused from excessive mechanical stress when changing the nozzle or improperly tightened screws (two) mounting the hotend to the extruder. 

Fixed by replacing the hotend or just the heatbreak. You can try to straighten it but there's danger of breaking.

To avoid always hold the heatblock firmly with wrench or plies while tightening the nozzle. Don't overtighten the mounting screws and screw them in little by little alternating between the two.

[Reddit post with the issue](https://www.reddit.com/r/Sovol/comments/10vi5j0/hot_end_not_level_is_this_normal_got_the_feeling/)

## Noisy bearings

The gravelly sound when the bearings are travelling over the linear rods is caused by Sovol sending out dry, unlubricated bearings. 

Quick fix is [lubricating the rods](/first-steps/#lube-linear-rods). Best fix is packing them with grease as shown by [lost in tech](https://www.youtube.com/@foundintech) and [SavageLau](https://www.youtube.com/@SavageLau):

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/6-iKoJXXwnM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/lUvaA4fJWH0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Motor mounts not 90°

Motors aren't at a true 90° angle to the frame due to mounts. This occurs on Z-axis and Y-axis motor mounts. 

You can try to bend the bracket but that requires some disassembly. As a quick fix print [this shim](https://www.printables.com/model/360276) and mount it between the motor and the extrusion.

![Shim the motor mount](/images/troubleshooting/motor_not_true.webp)

## Official SV06 Help Center

More common issues at the  [Official SV06 Help Center](https://sovol3d.com/blogs/news/help-center-sv06)
