---
comments: true
title: Add LED lights to SV06 extruder
description: Add lights to the SV06 (Plus) extruder to easier inspect the print and nozzle.
---

You've seen [SV07](https://sovol3d.com/products/sovol-sv07-klipper-direct-drive-3d-printer-print-speed-250mm-s?sca_ref=3309524.Vd4MGn0pGL&sca_source=sovol) LED light and now you're jealous? No need for that anymore!

!!! warning "This modification doesn't work with stock part cooling fan" 
    You need to [upgrade the fan](/Upgrades/cooling-upgrades.md) to a different orientation.

You will need the following to build your own nozzle LED:
1. 5V COB 320/m natural white LED strip: [Amazon](https://www.amazon.com/Powered-Density-Backlight-Bedroom-Lighting/dp/B0BK8MJF6W?crid=30T5GXQ6U5ML&keywords=5v%2Bcob%2Bled%2B320&qid=1683997218&sprefix=5v%2Bcob%2Bled%2B320%2Caps%2C186&sr=8-25&th=1&linkCode=ll1&tag=blakadders-20&linkId=622711267f67e3dd7ee4cd798b88db39&language=en_US&ref_=as_li_ss_tl), [AliExpress](https://www.aliexpress.com/item/1005003307581709.html?aff_fcid=e81223618e5d438eb4eb150dc91dbdf4-1683997769400-03610-_DkUXSZ3&tt=CPS_NORMAL&aff_fsk=_DkUXSZ3&aff_platform=shareComponent-detail&sk=_DkUXSZ3&aff_trace_key=e81223618e5d438eb4eb150dc91dbdf4-1683997769400-03610-_DkUXSZ3&terminal_id=3f8c776975fd455ba956809c02d71a91&afSmartRedirect=y)
2. JST 1.25 3-pin male connector with wires: [AliExpress](https://www.aliexpress.com/item/1005002332868366.html?aff_fcid=bf906959668142fbaa9e87880fb37b25-1683997737882-05066-_Dkbww29&tt=CPS_NORMAL&aff_fsk=_Dkbww29&aff_platform=shareComponent-detail&sk=_Dkbww29&aff_trace_key=bf906959668142fbaa9e87880fb37b25-1683997737882-05066-_Dkbww29&terminal_id=3f8c776975fd455ba956809c02d71a91&afSmartRedirect=y)
3. Soldering iron and solder

Print the LED strip mount from [Printables](https://www.printables.com/model/452216-sv06-plus-vortex-v2-adjustable-cooling-led-system/files)(Only the LED Mount STL file). It is recommended to print it with ASA or PETG.

Cut a piece of the LED strip that fits the LED mount. My LED strip had the copper tabs spaced exactly to length.

![cut a piece from LED ](/images/upgrades/led_cut.jpg)

Solder the wire with JST 1.25 connector to the led strip. When it is plugged into the extruder board the top pin is 5V, middle is GND and bottom is not used by the LED strip. You can remove the bottom wire from the connector since it is not needed.

![LED strip piece soldered](/images/upgrades/led_piece.jpg)

Mount the LED mount using original screws and stick the LED strip to it.

![LED mount mounting](/images/upgrades/led_mount.jpg)

Connect the LED to the empty plug at the right side of the extruder board.

![LED plug](/images/upgrades/led_plug.jpg)

Route the wire behind the screw post so it's not in the way.

![LED wire routing](/images/upgrades/led_wire_route.jpg)

The LED strip is always on with the original firmware.

![LED mounted](/images/upgrades/led_mounted.jpg)

![LED mounted 2](/images/upgrades/led_mounted2.jpg)
