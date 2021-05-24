# Sharkhead Nvidia Jetson TX2 Orbitty Case
A 3D-printed portable case for the Nvidia Jetson TX2 on a [Connect Tech Orbitty Carrier board](https://connecttech.com/product/orbitty-carrier-for-nvidia-jetson-tx2-tx1/) for embedded applications (robotics, UAV,...). The case is designed to be portable and easily moved between supports thanks to its clipping mechanism.


<img src="/documentation/pictures/render_2.png" align="center" width="600"/>


It is the ideal case for use as a onboard computer on a robot or UAV (careful: rapid unscheduled dissassembly on impact feature included). Free to use for academic and personnal (non-profit) use. Commercial use is not permitted without consent.

<a href="/documentation/pictures/4wd_holonomic_robot.png"><img src="/documentation/pictures/4wd_holonomic_robot.png" align="center" height="306" width="355"></a>
<img src="/documentation/pictures/foxtech_uav.png" align="center" height="306" width="421"/>

*The Sharkhead case mounted on an holonomic mecanum wheel robot and on a drone.*


## Overview
### Power requirements
The case integrates its own power supply regulation (LM2596 DC-DC step-down voltage regulator board) and can be directly plugged to a battery within the range of what's permitted by the LM2596 board (input voltage up to 40V, minimum 9V). In addition the case includes another voltage regulator to output power for an accessory, with adjustable voltage and up to 3A output load current.

<img src="/documentation/pictures/connector_back_side.png" width="450">

### Ports
The case exposes all the ports from the Orbitty Carrier board, including the GPIO and with the exception of the SD card port:
* Ethernet
* USB3
* HDMI
* micro-USB

<img src="/documentation/pictures/connector_left_side.png" width="550">

On the right side the RECOVERY, RESET and POWER buttons can be accessed, as well as the fan setting switches.


<img src="/documentation/pictures/buttons_right_side.png" width="550">

#### GPIO
The GPIO are forwarded to the female header on the side of the case.

<img src="/documentation/pictures/gpio_details.png" width="450">

## Assembly instructions
### Necessary parts
The following parts are required to assemble the case.

<img src="/documentation/pictures/assembly/assembly_all.png" width="700">

#### Printed part
* [(1x) lower case part (PLA)](/STL/casing_lower_part.STL)
* [(1x) connector block (PLA)](/STL/casing_connector_block.STL)
* [(1x) left clip (PLA)](/STL/clip.STL)
* [(1x) right clip (PLA)](/STL/clip.STL) (same as left clip)
* [(2x) front clips (PLA)](/STL/front_clip.STL)
* [(2x) rear locks (PLA)](/STL/lock.STL)
* [(1x) holder (PLA)](/STL/case_holder.STL)
* [(1x) case top cover (clear resin)](/STL/casing_upper_part.STL)

#### Mechanical parts
* (3x) M3 inserts (M4 outer diameter)
* (2x) M3 20mm male to female spacers
* (2x) M3 5-to-15mm hex head screws
* (5x) M3 18mm countersunk screws
#### Electronics
* (1x) NVidia TX2 or TX1 (of course)
* (1x) [Connect Tech Orbitty carrier board](https://connecttech.com/product/orbitty-carrier-for-nvidia-jetson-tx2-tx1/)
* (1x) set of antenna (included with the Orbitty carrier board)
* (2x) voltage regulator (step-down) LM2596 boards. The boards are cheap and easily findable online, but they should have the following dimensions to fit within the case.

<a><img src="/documentation/pictures/lm2596_board.jpg" height="300" width="300"/></a>
<img src="/documentation/pictures/lm2596_dimensions.png" height="300"/>

#### Connectors
The following connectors are needed for one case:
* (1x) XT60 male battery connector (or any battery connector)
* (1x) Molex minifit Jr. male housing (2x1) and its associated crimp terminals
* (2x) Ribbon cable female connectors (20 poles, 2.54mm) and associated 20 wire ribbon cable

### Printing the case
#### PLA
Most parts were printed using Ultimaker black PLA and/or black tough PLA with PVA supports (dual-printcore printer). The PVA support material is disovable in water and allow for a high precision in the printed connector housings. It's probably possible to print the parts without the PVA support material, but that would require more post-processing to remove the supports from the connector housings.

The following printing parameters were used for all parts printed in PLA:

| Parameter | Value |
| --------- | ----- |
| Layer height | 0.1mm |
| Infill | 40% |
| Infill pattern | cubic subdivision |
| Support material | PVA |
| Support pattern | triangles |
| Support overhang | 45% |

**front clip, left clip, right clip, rear locks**

For the clips, it's important to print them laying on their side to make the part stronger in the bending direction.
<img src="/documentation/pictures/clip_printing.png" align="center" height="475" width="652"/>


#### Clear resin
The cover is printed using a resin printer and clear resin so that the part is clear enough to see the LEDs (after sanding and coating). The resin used was the Formlabs Clear Resin V2 (FLGPCL02) but any clear resin can do.

**Post-process**

After printing, the part is rinsed of the remaining resin by immersion in a isopropyl alcohol bath as recommended by the [manufacturer](https://formlabs.com/blog/design-to-3d-print-form-3-workflow-video/), but the part is not cured afterward. Instead, it can be polished with sand paper and coated with a transparent paint to obtain a clear result ([check Formlabs blog article on clear parts here](https://formlabs.com/blog/3d-printing-transparent-parts-techniques-for-finishing-clear-resin/)).

<img src="/documentation/pictures/assembly/cover_print.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/cover_print2.JPG" align="center" width="390"/>

*The cover straight from the printer and after supports have removed and part has been rinsed.*

<img src="/documentation/pictures/assembly/cover_print3.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/cover_print4.JPG" align="center" width="390"/>

*Sanding the part and spray painting it with transparent paint makes it clear enough to see through*

### Putting it together

* Put the insert in the holes. If too tight, heat from a soldering iron can be applied (gently) to melt the inserts into position

<img src="/documentation/pictures/assembly/assembly1.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly2.JPG" align="center" width="390"/> 

* Solder the power supply wires to the DC-DC converters input.

<img src="/documentation/pictures/assembly/assembly3.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly4.JPG" align="center" width="390"/>

* Use a short lenght of wire to bridge the input from the lower converter to the upper one. Use the spacers to get an idea of the distance between the converters. The lower converter will provide power to the TX2 will the upper one will provide power the optional accessory output.

<img src="/documentation/pictures/assembly/assembly5.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly7.JPG" align="center" width="390"/>

* Solder the wires from the converter outputs. Cut the input cable at desired length and solder the XT-60 (or other) battery connector.

<img src="/documentation/pictures/assembly/assembly8.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly6.JPG" align="center" width="390"/>

* It's the good time to connect a battery and adjust the input voltage of the TX2. According to Connectech, the Orbitty carrier board take 9-14V as input voltage. Screw the converter's spacers into their inserts.

<img src="/documentation/pictures/assembly/assembly9.JPG" align="center" width="390"/>

* Crimp minifit connector pins to the upper converter output after adjusting length of the wires (the connector should slide in the output connector casing). Add connetor on the pins. Be sure to respect the polarity.

<img src="/documentation/pictures/assembly/assembly10.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly11.JPG" align="center" width="390"/>

* Push the connector into its casing to lock into place. If needed, use zip ties to lock the wires into place.

<img src="/documentation/pictures/assembly/assembly12.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly13.JPG" align="center" width="390"/>

* The lower converter output wires should run parallel to the case power supply cable. If needed, use zip ties to lock them into place.

<img src="/documentation/pictures/assembly/assembly13_2.JPG" align="center" width="390"/>

* Cut a ribbon length of 10cm (~4 inches) and crimp the connector on it according to picture orientation

<img src="/documentation/pictures/assembly/assembly15.JPG" align="center" width="390"/>

* Place one end of the assembled cable in the connector casing (respection orientation in picture) and push to lock in place.

<img src="/documentation/pictures/assembly/assembly16.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly17.JPG" align="center" width="390"/>

* Add the antenna connector on the back and screw them in place. 

<img src="/documentation/pictures/assembly/assembly21.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly19.JPG" align="center" width="390"/>

* The antenna wires can be folded and zipped in place. The tip of the wires might have to be bent a bit to give the TX2 enough space to slide in.

<img src="/documentation/pictures/assembly/assembly22.JPG" align="center" width="390"/>

* Place the TX2. Adjust the converter output wire lengths and screw them into the block terminal.

<img src="/documentation/pictures/assembly/assembly23.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly24.JPG" align="center" width="390"/>

* Connect the antenna to the TX2 (using a flat screwdriver if needed).

<img src="/documentation/pictures/assembly/assembly25.JPG" align="center" width="390"/>

* Connect the flat ribbon cable other end to the TX2 GPIOs, respecting orientation in picture.

<img src="/documentation/pictures/assembly/assembly26.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly27.JPG" align="center" width="390"/>

* Gently push the TX2 into place. Screw the top converter to the spacers using the M3 5-to-15mm hex head screws.

<img src="/documentation/pictures/assembly/assembly28.JPG" align="center" width="390"/>

* Turn the case upside down and screw the TX2 using the M3 18mm countersunk screws.

<img src="/documentation/pictures/assembly/assembly31.JPG" align="center" width="390"/>

* Add the rear locks and push them in place strongly.

<img src="/documentation/pictures/assembly/assembly32.JPG" align="center" width="390"/>

* Add the left and right clips and push them in place strongly.

<img src="/documentation/pictures/assembly/assembly33.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly34.JPG" align="center" width="390"/>

* Slide the TX2 connector block in place

<img src="/documentation/pictures/assembly/assembly35.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly36.JPG" align="center" width="390"/>

* Add the cover by first putting the front latch in place and then sliding it gently in place (the front latch is a weak point that I'm aware of).

<img src="/documentation/pictures/assembly/assembly37.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly38.JPG" align="center" width="390"/>

* Screw the cover in place using the remaining M3 18mm countersunk screw.

<img src="/documentation/pictures/assembly/assembly39.JPG" align="center" width="390"/>

* Screw the antennas.

<img src="/documentation/pictures/assembly/assembly40.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly41.JPG" align="center" width="390"/>

* Add the front clips on the holder part. If needed use a plier to secure them in place.

<img src="/documentation/pictures/assembly/assembly42.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly43.JPG" align="center" width="390"/>

* Put the case on the holder by sliding the rear locks in and pushing on the front until the clips get in place.

<img src="/documentation/pictures/assembly/assembly44.JPG" align="center" width="390"/> <img src="/documentation/pictures/assembly/assembly45.JPG" align="center" width="390"/>

* Assembly is done!

<img src="/documentation/pictures/assembly/assembly46.JPG" align="center" width="600"/>
