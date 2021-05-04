# Sharkhead Nvidia Jetson TX2 Orbitty Case
A portable case for the Nvidia Jetson TX2 on a [Connect Tech Orbitty Carrier board](https://connecttech.com/product/orbitty-carrier-for-nvidia-jetson-tx2-tx1/) for embedded applications (robotics, UAV,...). The case is designed to be portable and easily moved between supports thanks to its clipping mechanism.

It is the ideal case for use as a onboard computer on a robot or UAV.

ADD PICTURE OF EXAMPLE.

Free to use for academic and personnal (non-profit) use. Commercial use is not permitted without consent.

## Overview
### Power requirements
The case integrates its own power supply regulation (LM2596 DC-DC step-down voltage regulator board) and can be directly plugged to a battery within the range of what's permitted by the LM2596 board (input voltage up to 40V, minimum 9V). In addition the case includes another voltage regulator to output power for an accessory, with adjustable voltage and up to 3A output load current.

### Ports
The case exposes all the ports from the Orbitty Carrier board, including the GPIO and with the exception of the SD card port:
* Ethernet
* USB3
* HDMI
* micro-USB

#### GPIO
The GPIO are forwarded to the female header on the side of the case.

ADD PICTURE OF GPIO ON CASE

## Assembly instructions
### Necessary parts
The following parts are required to assemble the case.

ADD PICTURE ALL PARTS ON DESK

#### Mechanical parts
* (3x) M3 inserts (M4 outer diameter)
* (2x) M3 20mm male to female spacers
* (2x) M3 5-to-15mm hex head screws
* (4x) M3 18mm countersunk screws
#### Electronics
* (1x) NVidia TX2 or TX1 (of course)
* (1x) [Connect Tech Orbitty carrier board](https://connecttech.com/product/orbitty-carrier-for-nvidia-jetson-tx2-tx1/)
* (1x) set of antenna (included with the Orbitty carrier board)
* (2x) voltage regulator (step-down) LM2596 boards. The boards are cheap and easily findable online, but they should have the following dimensions to fit within the case.

ADD PIC DIMENSIONS

#### Connectors
The following connectors are needed for one case:
* (1x) XT60 male battery connector (or any battery connector)
* (1x) Molex minifit Jr. male housing (2x1) and its associated crimp terminals
* (2x) Ribbon cable female connectors (20 poles, 2.54mm) and associated 20 wire ribbon cable


### Printing the case
### 
