# Mirage

## Foreword
Custom PCB board inspired by the [#badgelife](https://www.youtube.com/watch?v=G2fHKRONc6U) and PCB Art movement. The "Mirage" badge represents to me a kind of miracle because it demonstrates that without prior knowledge, thanks to all the available free information out there, it is possible to build systems from scratch and, on top of that, style them and express ourselves.

The art of the board itself is NOT done by me, it's all done by the wonderful [@OseanWorld](https://twitter.com/oseanworld). Huge props to Osean for keeping me and everyone in the community dreaming and doing art, and thanks for creating such a beautiful cyberspace.

## Directory Structure
As you can see, right now the repo is pretty unorganized. Maybe I'll restructure it in the future, but as of now here are the main files:

- **.kicad*: this files contain all the relevant design for the electrical part of the board. The **.kicad_pro** file is the main faile you'll want to open (by double clicking on it). The **.kicad_sch** contains the schematic for the board. The **kicad_pcb** contains the layout for the components and the overall PCB design.
- *nudeko.pretty*: contains the custom PCB outline, silkscreen and copper layers which done in Inkscape. **You'll have to load this module into your footprint library if KiCad doesn't do that automatically.**
