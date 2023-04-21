# Troubleshooting 

## General 3D Printer Troubleshooting

[Teaching Tech](https://teachingtechyt.github.io/troubleshooting.html) has a great resource about general 3D printer troubleshooting.

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

## Blue/Black/Blank Screen issue

[Reddit post](https://www.reddit.com/r/Sovol/comments/12686c3/how_to_troubleshoot_the_blueblackblank_issue_on/?utm_source=share&utm_medium=web2x&context=3)

## Heating Failed: Bed

![Heat Bed error symptom](/images/troubleshooting/heatbederrorissue.webp)

Could be a result of a failed thermistor or heat bed wires breaking. Inspect the wires and whether they're properly soldered to the heat bed.

[Official Sovol](https://forum.sovol3d.com/t/sv-06-heat-bed-causes-error/1564/2?u=blakadder) recommendation:

This might be caused by the corrupted connection wire. To test the wiring status, pls exchange the heating wire and thermistor connector of the hotbed on the main board to the position of nozzle’s.

![Heat Bed error](/images/troubleshooting/heatbederror.webp)

And then set the nozzle temp to 60 on the display and check if the hotbed is heating up to around 60. If the hotbed could be normally heated up, the heating wire and thermistor connector of the hotbed might be corrupted. If the hotbed would not heat up after you swap the wires, the hotbed is corrupted. In this case, please contact the CS at info@sovol3d.com for assistance.

## Poor extruding or extruder jammed 

It is common[^1][^2] that the set screw (grub screw) holding the extrusion gear to the extruder motor shaft got loose and is rubbing against or catching on the extruder chassis. This manifests in under extrusions, extruder motor skips and ultimately extruder getting jammed.

To fix or avoid the issue, first remove filament from the extruder. 

<figure markdown>
  ![Unscrew the extruder tensioner screw](/images/troubleshooting/extruder_screw1.webp)
  <figcaption>Unscrew the extruder tensioner screw</figcaption>
</figure>

<figure markdown>
  ![Rotate the extruder until you see the grub screw and tighten it](/images/troubleshooting/extruder_screw2.webp)
  <figcaption>Rotate the extruder until you see the grub screw and tighten it</figcaption>
</figure>

Optionally you can add a drop of thread locker (blue) or clear nail polish to secure it. This might make future disassembly harder.

<figure markdown>
  ![Grub screw needs to hold the shaft at the marked spot](/images/troubleshooting/extruder_screw3.webp)
  <figcaption>Grub screw needs to grip the extruder shaft at the marked spot</figcaption>
</figure>

If you spot metal shavings you will need to [disassemble the extruder](https://youtu.be/mFIRd1ZH81I) and thoroughly clean it. If there is damage contact [Sovol support](https://sovol3d.com/pages/contact-us) and ask for a replacement.

## Dry noisy bearings 

The gravelly sound when the print head is travelling is caused by Sovol sending out dry, unlubricated bearings. Best solution is packing them with grease as shown by [lost in tech](https://www.youtube.com/@foundintech) and [SavageLau](https://www.youtube.com/@SavageLau):

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/6-iKoJXXwnM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/lUvaA4fJWH0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Y-axis carriage warped

<https://www.reddit.com/r/Sovol/comments/113ba83/sv06_y_carriage_warped/>

## Official SV06 Help Center

More troubleshooting at the  [Official SV06 Help Center](https://sovol3d.com/blogs/news/help-center-sv06)

[^1]: [Source]([https://www.reddit.com/r/Sovol/comments/1144lhc/solved_sv06_gear_stuck/](https://www.reddit.com/r/Sovol/comments/12bewzn/sv06_psa_check_your_extruder_and_apply/))
[^2]: [Source](https://www.reddit.com/r/Sovol/comments/1144lhc/solved_sv06_gear_stuck/)
