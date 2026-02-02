Eric Hazen's contact is hazen@bu.edu. Some easy designers are:
- https://easyeda.com/ (cloud software)
- https://www.kicad.org/ (developed by CERN)
- Altium, Cadence, and Mentor (paid options)

A PCB is good for permanent, reliable interconnection of components that's super easy to manufacture. Ideally you're supposed to test and simulate on a breadboard before you go to actual PCBs. Pick a software from above, pick components for the PCB iteration (acquire models). 

Design the physical enclosure of the PCB before doing the layout. Draw the schematics and place the component footprints and route the connections in the PCB editor
## Selection
### Mounting (THT, SMT)
The old way to do it were putting components to do THT, impaling the circuit through the board and soldering the back. But starting in the 1980s, SMT was introduced to stop hole drilling. THT is easier to solder and can handle higher power, but fewer modern parts are available.
### Layering (2 vs 4+)
Most projects should use 4-layer boards: two inner, front and back. But they used to make two-sided boards. They'll run you about $30. More layers means more interconnecting. Having ground is really helpful, so one layer might be used just for ground.
### Components
Make sure to use proper wattage (resistors), voltage (capacitors) and current (inductors). For SMT, use 1206 or 0805, but as SMT is, it's hard to solder. For Thru-hole, pick the ones with colored bands (.4 or .5 in pin spacing). For ICs, use SOIC or TQFP for SMT and DIP packages for Thru-hole. Don't use QFN, BGA, or DFN. 
### Modules
Modules are always fun to work with, so use ones without screw terminals. You can just put headers on a module and then attach it to the correct port. 
### Part Models
You need symbols (schematic), footprints (layout), and 3D models (enclosure). It can usually found inside the CAD tool libraries, or DigiKey or Mouser websites. For KiCAD, you have the footprint assignment tool to assign symbols with footprints.
## Drawings
PCB design is accomplished using CAD tools to create designs or artwork. Schematics are for humans to read and the layout is for what's actually made. The schematic should be neat and easy for the humans to read:
- no wire crossing
- left-to-right
- GND (down) and VDD (up) symbols used everywhere
- comment the unobvious and note the part values
- capacitive filter for power pins (10-100 nF)
- transistors should be pointed vertically, with current going up to down\
- T junctions only (but what about)

Connectors usually have 2.54 mms for space for headers. There are terminals, transistors, packages, etc. Make sure to note the pin order (GDS vs DGS). The schematic to footprint is an easy conversion, pin for pin. If there's a part with multiple amplifiers or gates, make sure to copy them as well.
## Board Setup
Use 4-layer boards using the KiCAD layer count. For Design Rules/Net Classes, have some guideline minimums:
- 0.2 mm clearance
- 0.2 mm min. width (go up if more current)
- 0.8 mm via size 
- 0.4 mm via holes

Some general layout considerations are to place connectors and controls so they fit well physically. Then you can attach all the devices with connectors to the PCB. **Always put mounting holes and make them big enough!** Attach properties for DigiKey numbers so you can generate a bill of materials.

To reiterate:
1. Create an outline (a rectangle)
2. Import parts from schematic
3. Organize parts within the board outline

For step 3, **use a 0.5 mm grid!** Place the mechanically-important parts first like switches, buttons, holes and connectors so you don't screw up physically. Place filter capacitors near the power pins and other related components next to each other (but not too close). Then, you can make a 3D model.
## Routing
Select the routing tool and select one end and then select the other with intermediate points. Hit a key to change your layer. Have one layer set to horizontal and the other for vertical traces. For the widths themselves consider the following currents:
- 0.050 in for 3.0 A
- 0.016 in for 1.0 A
- 0.007 in for 0.5 A

For GND (green) and VDD, you can set an entire layer as such using the "Filled Zone" tool. Make sure to set connections to "Thermal Reliefs" or else bad things will happen. Then, draw the biggest rectangle you can. Then, "Edit -> Fill All Zones" to fill it all in, but you still need to connect any SMT pads yourself (vias, but don't put them through the pads for THT). If you have multiple power supplies, you can create a zone for one and a zone for the other.
## Models
It's easiest to use models supplied by the tool, but you can also get models from UltraLibrarian or Snap Magic, but they might not be as correct. The tutorial for KiCad is here: https://docs.kicad.org/9.0/en/getting_started_in_kicad/getting_started_in_kicad.html

## Manufacturing
![[Pasted image 20260130141111.png]]
To ink, just be reasonable with it. Gerber files can be made as .gcode files which can be sent over to manufacturers. To access this, you can click the Plot function. Then generate drill files and put it all in a zip. Go here to order it: [JLCPCB.com](). Shipping might suck, but the tariffs are even worse. Talk to your advisor or budgeter if you don't want to use your credit card. 

## Electrical Safety
![[Pasted image 20260130141254.png]]
1. 50 volts is considered high voltage. I guess 24 volts is safe enough. 
2. Turn off power and unplug AC powered equipment before servicing. 
3. All AC wiring in any device must be enclosed to prevent contact. 
4. When working with AC, keep one hand behind your back and use insulated tools.
5. Keep your workspace clear of other materials.
6. **Never modify wiring** when connected to power.
7. Keep water away from electricity.
8. Check circuits for proper grounding.
9. Use a fuse just once

Don't use LiPo batteries if you can just use Lithium Ion batteries. 4 AA batteries also work pretty nicely. AC power through bricks are also fun. Just don't use LiPo man...

When working with AC power:
- Avoid AC power.
- Always ensure AC wiring is insulated and enclosed.
- Always ground exposed metal.
- Always have a fuse be the first thing the AC source sees.

Get a book from Harvard called ART of ELECTRONICS.