# Sharkhead Nvidia Jetson TX2 Orbitty Case
A 3D-printed portable case for the Nvidia Jetson TX2 on a [Connect Tech Orbitty Carrier board](https://connecttech.com/product/orbitty-carrier-for-nvidia-jetson-tx2-tx1/) for embedded applications (robotics, UAV,...). The case is designed to be portable and easily moved between supports thanks to its clipping mechanism.


<img src="/documentation/pictures/render_2.png" align="center" width="600"/>


It is the ideal case for use as a onboard computer on a robot or UAV (rapid unscheduled dissassembly on impact feature included). Free to use for academic and personnal (non-profit) use. Commercial use is not permitted without consent.

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

ADD PICTURE OF GPIO ON CASE

## Assembly instructions
### Necessary parts
The following parts are required to assemble the case.

ADD PICTURE ALL PARTS ON DESK

#### Printed part
* (1x) lower case part (PLA)
* (1x) connector holder (PLA)
* (1x) left clip (PLA)
* (1x) right clip (PLA)
* (2x) front clips (PLA)
* (2x) rear locks (PLA)
* (1x) holder (PLA)
* (1x) case top cover (clear resin)

(ADD link to STL files)

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

