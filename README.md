
iCAD Component Library

Scope
This document should be a general guide for common setup of KiCAD component library supporting
PCB design process.
Overview
The component library in general consits of two parts a schematic symbol and a footprint.
The schematic symbol also contains attributes like: ordering information, description and the assigned footprint. 
All parts created for ES library are created first in a temporary location ( project library ) and are transfered before official releasing project data.

Server
The component library is read only and can be found on internal SHL server: Path: L:\Component_Data.
EESCHEMA schematic editor: L:\Component_Data\01_LIB_SCH
PCBNEW layout editor: L:\Component_Data\02_LIB_PCB
If new components are created it is recommended to store them in a local project library which can be transfered by admin later.
Symbol
To draw and edit a symbol we are using "Symbol library editor".

The two examples below are a good example for the two most important symbol design rules.
    1. Atomic Parts
Atomic parts fully define a component, specifying a matching footprint, and are named based on the MPN (manufacturer part number).
Atomic parts are ready to be placed onto the PCB as they are already associated with a footprint.
    2. Pin transparency
Pin transparency means all pins, pads a physical component have should be shown on the schematic even if they have no function
like test pins or non connected pins. 
    3. Symbol name
The symbol name must be unique and follow the manufacturer name or product series. For passive components the component
can be also named like: "value+ManufacturerSeries+footprint".
    4. Field properties
Every schematic symbol has field with attributes which belong to the symbol.
    5. Pin numbering/naming
Pin numbering and naming need to follow the component manufacturer datasheet. If a component
has alternative pin function there can be also 2 symbol for one component (I2C/SPI).
