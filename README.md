# tiny-m-build

## WORK IN PROGRESS

This is my particular spin on the Tiny-M build, a variant of the Voron V0 using Mitsumi 2020 Extrusions and Nema 17 motors.  The Voron machines are home build high performance printers. With the V0 being the smallest of the series. The numbering scheme, V0, V1, V2 represent different machines, so don't get confused that's it's a revision.

Since I've not started the build yet, the first things I'll link are the Voron V0 build and the Tiny-M repo.
I'd like to use a small direct hot end instead of the standard Voron V0 Boden so that it will easily print flexable material.
In addition, I really like the two position hinged TopHat by hartk1213

First off, there is a very active Discord channel for VoronDesign. The users are really helpful and friendly which for a home build
3d printer is a huge win.

Voron V0 - https://vorondesign.com/voron0

Tiny-M https://github.com/gsl12/Tiny-M

Sherpa Mini-Extruder https://github.com/Annex-Engineering/Sherpa_Mini-Extruder

Hinged Top Hat - https://github.com/hartk1213/VoronUsers/tree/master/printer_mods%2Fhartk1213%2FVoron0_Hinged_Top_Hat

motion controller - BIGTREETECH SKR Mini E3 V2.0 New Upgrade Control Board 32Bit with TMC2209 

job control - Raspberry Pi 3 or 4?

T8x4 ptfe coated Lead Screw + POM - 215mm	 *Note: may have to cut to length as this isn't standard.

all images so far from Xile on Voron group on discord


## My preliminary BOM
https://docs.google.com/spreadsheets/d/1UV62ADl2gtK5vL0fV1nwevR6O9Ppzs0MBe7jnsI-jo4/edit?usp=sharing

## Build Platform + Plate Information
The build plate should be either ATP-5 or MIC6 Cast Aluminum 6" x 6" x 1/4" which is about 150mm x 150mm x 6mm onto which a magnetic layer is added, topped with a spring steel build plate.

The heater for the bed should be aprox 0.4 watts/cm^2.  So 15cm x 15cm = 255cm^2    255 * 0.4 = 102 watts. Less power will heat slower, more might be ok, but don't go crazy.  See the following for great info https://duet3d.dozuki.com/Wiki/Choosing_a_bed_heater


## Stepper Motor Light Reading
Many Nema 17 will fit into the space. 
https://duet3d.dozuki.com/Wiki/Choosing_and_connecting_stepper_motors

## Frame Assembly
Depending on if you are drilling + tapping for your rails or using the 90 degree internal connectors (or possibly both!)

If you are drilling (and have a printer) you can make a guide:
See the STL drill template for the holes: 10, 36 and 60

The bottom extrusions have 50mm of space to the bottom of the uprights.
The back is 26mm on the side beams for a total of 26mm + 20mm total (from the back beam).

## Hinged TopHat
I really like the way the hinged TopHat works and the two positions it can stay in
Need to determine the # of Mitsumu 2020 beams to order. There is a 2020 TopHat for V0 that I've patterned the following on
(was at https://github.com/gsl12/Tiny-M/tree/master/STLs/usermods/2020_Hinged_TopHat_Print)

The following measurements have not been verified in an actual build.
Verticals
Back 2 x 75 mm
Front 2 x 92 mm 

Horizontal
Front 2 x 260 mm
Back 1 x 260 mm, 1 x 274 mm

Sides
Top Right/Left 2 x 260 mm 
Bottome Right/Left 2 x 230 mm

Totals 
2 x 75 mm
2 x 92 mm
2 x 230 mm
5 x 260 mm
1 x 274 mm

### Software

Thinking of using Raspberry Pi 3 (or 4) with Mainsail OS and Klipper on BTT SKR Mini E3 V2

## Mainsail OS
https://github.com/raymondh2/MainsailOS/releases

How to install
https://www.youtube.com/watch?v=MK0-MDVJG94

How to configure mainsail
https://meteyou.github.io/mainsail/setup/

Configuration of SKR Mini E3 V2 for klipper
https://github.com/KevinOConnor/klipper/blob/master/config/generic-bigtreetech-skr-mini-e3-v2.0.cfg

