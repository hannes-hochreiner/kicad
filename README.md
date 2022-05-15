# kicad
Custom KiCAD components

## Organization
The different artifacts for the components are organized in four folders:
  * footprints
  * models
  * sheets
  * symbols

### Footprints
Contains the component footprints.
Components from one manufacturer are combines into one library.
Hence, the structure of the folder is:
```
  footprints/h0h4_<manufacturer>.pretty/<component part number>.kicad_mod
```

### Models
Contains 3D models of the components.
For me, it was easiest to use FreeCAD to draw the components.
For the import into KiCAD, I exported the drawings to the step format.
The structure of the folder is:
```
  models/h0h4_<manufacturer>/<component part number>.{fcstd,step}
```
### Sheets
This folder contains sheets that can be imported into new designs.
The idea is to have common building blocks for more complex components.
For example, an MCU needs decoupling capacitors, a reset button, a programming interface, and external oscillators.
All these parts can be put on a sheet, so in a new design the complete set can be imported and then modified.
The structure of the folder is:
```
  sheets/<manufacturer|module class>/<part number>.{pro,sch}
```
### Symbols
Contains a symbol for each manufacturer.
Inside each library, the symbols for the manufacturer's parts are stored.
The structure of the folder is:
```
  symbols/<manufacturer>.{dcm,lib}
```

[![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Some parts were obtained and/or derived from [SnapEDA](https://www.snapeda.com/).
