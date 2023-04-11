# Troubleshooting 

## Blue Screen

The bootloader on the 32bit controller boards **requires** FAT32 format and can not use any other formats.

[Official Sovol](https://forum.sovol3d.com/t/new-sv06-failed-first-print-and-now-blue-screen/1791/2?u=blakadder) recommendation

Here’s what the engineer suggests to rule out the bluescreen issues. I hope this helps! Let me know if you have any other questions.

1. Remove the screen and operate it on the table as static interference may be causing the issue.
2. Refer to the video and refresh the stock firmware. Before updating the firmware, please format the memory card by following these steps.
  1. Press the Win+R key to open the command prompt;
  2. Enter “cmd” and press Enter;
  3. Enter “format/q H:/fs:fat32/a:4096” (note that “H” is the disk name of the memory card, please make sure to confirm the disk number of your memory card).
3. Flash [latest firmware](https://sovol3d.com/pages/download)

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/p6l253OJa34" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Blue/Black/Blank Screen issue

[Reddit post](https://www.reddit.com/r/Sovol/comments/12686c3/how_to_troubleshoot_the_blueblackblank_issue_on/?utm_source=share&utm_medium=web2x&context=3)

## Heating Failed: Bed

![Heat Bed error symptom](/images/troubleshooting/heatbederrorissue.webp)

Could be a result of a failed thermistor or heat bed wires breaking. Inspect the wires and whether they're properly soldered to the heat bed.

[Official Sovol](https://forum.sovol3d.com/t/sv-06-heat-bed-causes-error/1564/2?u=blakadder) recommendation:

This might be caused by the corrupted connection wire. To test the wiring status, pls exchange the heating wire and thermistor connector of the hotbed on the main board to the position of nozzle’s.

![Heat Bed error](/images/troubleshooting/heatbederror.webp)

And then set the nozzle temp to 60 on the display and check if the hotbed is heating up to around 60. If the hotbed could be normally heated up, the heating wire and thermistor connector of the hotbed might be corrupted. If the hotbed would not heat up after you swap the wires, the hotbed is corrupted. In this case, please contact the CS at info@sovol3d.com for assistance.

## Poor extruding or extruder jammed 

It is common[^1][^2] that the set screw (grub screw) holding the extrusion gear to the extruder motor shaft got loose and is rubbing against or catching on the extruder chassis. This manifests in under extrusions, extruder motor skips and ultimately extruder getting jamed.

<figure markdown>
  ![Grub screw loose damage](/images/troubleshooting/loosesetscrew.webp)
  <figcaption>Damage caused by loose set screw</figcaption>
</figure>

Remove filament from the extruder. Unscrew the extruder tension adjuster screw which holds the extruder lever. Now you can drop down the lever and look inside. Rotate the extruder knob until you can see the set screw. Tighten it up. Optionally you can add a drop of thread locker or clear nail polish to secure it. This might make future disassembly harder.

## Dry noisy bearings 

The gravelly sound when the print head is travelling is caused by Sovol sending out dry, unlubricated bearings. Best solution is packing them with grease as shown by [SavageLau](https://www.youtube.com/@SavageLau):

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/lUvaA4fJWH0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

[^1]: [Source]([https://www.reddit.com/r/Sovol/comments/1144lhc/solved_sv06_gear_stuck/](https://www.reddit.com/r/Sovol/comments/12bewzn/sv06_psa_check_your_extruder_and_apply/))
[^2]: [Source](https://www.reddit.com/r/Sovol/comments/1144lhc/solved_sv06_gear_stuck/)
