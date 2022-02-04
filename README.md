# Mirage

Custom PCB board inspired by the [#badgelife](https://www.youtube.com/watch?v=G2fHKRONc6U) and PCB Art movement. The "Mirage" badge represents to me a kind of miracle because it demonstrates that without prior knowledge, thanks to all the available free information out there, it is possible to build systems from scratch and, on top of that, style them and express ourselves.

![3D View](/refImages/3d.png)

The art of the board itself is NOT done by me, it's all done by the wonderful [@OseanWorld](https://twitter.com/oseanworld). Huge props to Osean for keeping me and everyone in the community dreaming and doing art, and thanks for creating such a beautiful cyberspace.

## Electronics

The modules and components used in this board are the following:
- ESP32-PICO-D4: MCU + BLE transciever.
- CP2102-GMR: USB-to-UART converter. Needed to upload code and debug via UART.
- S8050 NPN transistors: needed to detect automatically when code is being uploaded to the MCU. 
- AMS1117-3.3: 5V to 3.3V regulator.
- AO3401A P channel MOSFET: works as reverse polarity protection.
- USBLC6-2SC6: diode array for ESD protection.
- M7 Diode.
- USB Micro B connector.
- 3 push buttons.
- Shitload of capacitors, resistors, LEDs.

All the references and datasheets of the components used in the schematic can be found in the `/datasheets` directory.

If you want to learn the technicalities of designing a PCB yourself you can checkout [Phil's Lab youtube channel](https://www.youtube.com/c/PhilS94) for an intro to PCB design.

## Firmware

## Art
The art of this board was made entirely inside Inkscape and ported to KiCad thanks to the [svg2shenzhen](https://github.com/badgeek/svg2shenzhen) extension made by [@badgeek](https://github.com/badgeek). Also the great [video tutorial](https://www.youtube.com/watch?v=Sbkvza8cKQE) done by [@mrtwinkletwink](https://twitter.com/mrtwinkletwink) helped me a lot when it came to understand the different layers of the board and how to use svg2shenzhen in general.

![PCB View](/refImages/pcb.png)

## Directory Structure
As you can see, right now the repo is pretty unorganized. Maybe I'll restructure it in the future, but as of now here are the main files:

- **\*.kicad**: This files contain all the relevant design for the electrical part of the board. The *.kicad_pro* file is the main file you'll want to open (by double clicking on it). The *.kicad_sch* contains the schematic for the board. The *kicad_pcb* contains the layout for the components and the overall PCB design.
- **nudeko.pretty**: contains the custom PCB outline, silkscreen and copper layers which done in Inkscape. *You'll have to load this module into your footprint library if KiCad doesn't do that automatically.*
- **nudeko.svg**: This file contains the vector art. It was done in Inkscape and the document was prepared and imported to KiCad with the [svg2shenzhen](https://github.com/badgeek/svg2shenzhen) extension made by [@badgeek](https://github.com/badgeek).
- **symbols**: This directory contains a custom library I made for KiCad. It only contains the M7 diode footprint. If KiCad doesn't recognize this automatically you'll have to tell it where it's located.
- **nudekoINK2KICAD**: Contains the files generated by the svg2shenzhen extension. Might delete this in the future cause it only adds junk to the repo.
- **datasheets**: As its name implies, here are the datasheets of each component I used for the electronics (aside from passive components). You could use other components if you know what you're doing but this is what was in stock (or was a basic part for the most part) at [JLCPCB](https://jlcpcb.com/).
- **MirageR1-backups**: Generated automatically by KiCad. Might delete this guys too.

