# Summary
Marlin 2.0 Bugfix with changes for my Modded Ender-3 with SKR V1.3 and BLTouch v3.0.

# Changelist
June 4, 2022 - Changed to Screw-In stud thermistor (104GT-2) and copper block.

December 20, 2020 - Changed TriangleLabs Titan to TriangleLabs BMG.  Used this extruder mod: https://www.thingiverse.com/thing:3781222

October 2019 - Changed drivers out to TMC2209.  Setup and tuned Sensorless homing sensitivity

5/20/2019 - Been tweaking this a bit.  I played with the accelerations, but have decided just to stick with and copy the Prusa MK3 default acceleration settings.  I have enabled a hidden BLTouch HighSpeed mode, gone aggressive with BLTouch probing.  Also changed from Petsfang Titan Direct to this one: https://www.thingiverse.com/thing:3594559, and went with a 0.9 Deg LDO Extruder motor

4/20/2019 - Pretty happy with this config. Everything works, got some nice prints. Bltouch is centered enough.  Linear Advance on TMC2208 working (in spreadcycle on E) with the minimum pulse width fixes.  Probably just quality of life tweaks and tuning from here onwards.  Such as filament load/unload length etc

4/12/2019 - Nozzle Fan had a separated wire, hardware problem.  
Fork is pretty much working and good to go, with exception that I want to center the BLTouch probing pattern.

4/5/2019 - Fork is working. Nozzle Fan is not working but need to test if its a hardware problem.
Other Known issues is that the BLTouch probing matrix is centered too far back on the bed, pretty close to the back edge.  Has something to do with home offsets or X/Y Minimum.

# Printer mods
This fork is meant for my Creality Ender-3 Modded machine with these properties/mods (Note: I bought the printer from [TallDonkey](https://github.com/talldonkey/Marlin-2.0-Ender-3-SKR-1.3) and he did all these cool mods!):

* Early Ender-3
* Stock Display (CR10STOCKDISPLAY) using single ribbon cable
* Bigreetech SKR V1.3 Mainboard (32-bit)
* Bigtreetech TMC2209 V1.2 on X, Y, Z and E via UART in Stealthchop
* Stock Creality Hotend with [TH3D Titanium All-Metal Heatbreak](https://www.th3dstudio.com/product/tough-titanium-heatbreak-for-creality-machines-tough-dual-hotend/)
* [Polisi3D Copper Heatblock](https://www.amazon.com/Temperature-Plated-Extruder-Creality-Printer/dp/B08NVTJM4S)
* [Trianglelab Swiss MK8 Hardened Steel Nozzle](https://www.aliexpress.com/item/2255800032773797.html)
* Screw-In stud thermistor (104GT-2)
* [Creality Direct Drive for Stock/Microswiss Hotend and BMG](https://www.thingiverse.com/thing:3781222)
* [Trianglelab BMG 2.0](https://www.aliexpress.com/item/3256803279640594.html)
* Original BLTouch V3.0 using the left-side mounted BLTouch mount with above
* [0.9 Degree LDO Pancake Extruder Motor from Printed Solid](https://www.printedsolid.com/products/ldo-nema-17-motor-pancake-ldo-42sth25-1404)
* Filament Runout Sensor (Lerdge)
* [Silicone Bed Spring Replacements](https://www.amazon.com/FYSETC-Printer-Heat-Resistant-Silicone-Creality/dp/B07M66KJNX)
* [FYSETC POM Lead Screw Nut](https://www.amazon.com/4-Pack-Printer-Trapezoid-Creality-Ender-3/dp/B0888DWRW8)
* [Arctic Silent 80mm PSU Fan](https://www.amazon.com/ARCTIC-Silent-inaudible-Configuration-ACFAN00245A/dp/B08WHMP2CD)
* Gates Belts on X and Y
* Double Magnetic Bed - Magnetic Sheet + [9 Neodynium N52 Magnets](https://www.aliexpress.com/item/2251832763110298.html)


Other Printed Mods:
* Belt Parallelism
  * [Y Axis Tensioner](https://www.thingiverse.com/thing:3097972)
  * [X Axis Tensioner with Straightned Belt Path](https://www.thingiverse.com/thing:3537042)
  * [X Belt Straigthener](https://www.thingiverse.com/thing:3288949)
  * [Y Axis Idler](https://www.thingiverse.com/thing:3136428)
* [80mm PSU Fan Cover](https://www.thingiverse.com/thing:3437190)

Miscelleanous Accessories:
* TheKiinngg Ender Textured Bed
* Glass Bed
* Double Sided Smooth PEI and BuildTak-Type Spring Steel Bed
* Spare Trianglelab Titan Extruder

# How to build
1) Install [VSCode + Platformio + Auto Build Marlin](https://marlinfw.org/docs/basics/install_platformio_vscode.html).
2) In `Auto Build Marlin`, build code. It will [generate](https://gulfcoast-robotics.com/pages/bigtreetech-skr-mini-e3-marlin-2-0-firmware) a `firmware.bin` file.
3) Copy this file to a micro SD card (Note: SD card must have an allocation size of 4096 bytes. If the SD card is too big, you will need to create a smaller partition in the card).
4) Insert the micro SD card to the 3D-Printer and reboot it.

# Disclaimer
This firmware is NOT maintained by Marlin. This is meant to be a personal fork/branch to contain my specific 3d printer configuration that will never be merged back upstream, but rather provides me the ability to make my own custom changes while merging in upstream Marlin 2.0.x updates.

# License
THIS IS PROVIDED UNDER THE GPL V3 LICENSE.
PROVIDED AS-IS. NO SUPPORT OR WARRANTY IS PROVIDED.
