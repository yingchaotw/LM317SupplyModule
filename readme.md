[![LM317 Supply Module](https://img.shields.io/static/v1?label=&message=LM317%20Supply%20Module&color=gray&logo=Github)](https://github.com/tw1chao/LM317SupplyModule)
[![license - CC BY-SA 4.0](https://img.shields.io/static/v1?label=license&message=CC+BY-SA+4.0&color=fcaabe)](https://creativecommons.org/licenses/by-sa/4.0/)
[![forks - LM317 Supply Module](https://img.shields.io/github/forks/tw1chao/LM317SupplyModule?style=social)](https://github.com/tw1chao/LM317SupplyModule/fork)
[![stars - LM317 Supply Module](https://img.shields.io/github/stars/tw1chao/LM317SupplyModule?style=social)](https://github.com/tw1chao/LM317SupplyModule/stargazers)

# LM317 Supply Module

Although I have a high-power power supply, it only provides a single channel of voltage. Since I require multiple voltage levels, I have decided to design an LDO supply module to regulate the voltage accordingly.
I envision the supply module to be assembled in a manner similar to Lego blocks, allowing for easy expansion and modification.

## Circuit

![](./Image/LM317%20Supply%20Module.jpg)

## PCB 3D View

![](./Image/LM317%20Supply%20Module%20PCB%203D.png)

### Bill Of Material
1. [PMOS - DMP4011SPSQ](https://www.diodes.com/part/view/DMP4011SPSQ/#tab-details)
2. [LDO - LM317](https://www.ti.com/product/LM317)
3. [SW SPDT - 5176A](https://kinsten.com.tw/index.php?route=product/product&product_id=49621&search=壓動開關5.8×5.8mm) / [TL2203EE](https://mou.sr/3LJwoE3)


## Toolchain

Use Open-Source free software to designed this project.

### KiCAD
[![KiCAD](https://img.shields.io/static/v1?label=KiCAD&color=2536A1&message=7.0.2-0&logo=KiCAD)](https://www.kicad.org/) 

KiCad (/ˈkiːˌkæd/ KEE-kad) is a free software suite for electronic design automation (EDA). It facilitates the design and simulation of electronic hardware. It features an integrated environment for schematic capture, PCB layout, manufacturing file viewing, ngspice-provided SPICE simulation, and engineering calculation. Tools exist within the package to create bill of materials, artwork, Gerber files, and 3D models of the PCB and its components. -- [Refer to Wiki](https://en.wikipedia.org/wiki/KiCad)

#### kicad V7.0.2 issue
When I run electrical rules checker, KiCAD show me [ERC report](./Circuit%20-%20LM317%20Supply%20Module/ERC-issue.rpt). This issue refer to [Error reading simulation model from symbol](https://gitlab.com/kicad/code/kicad/-/issues/14569).
about this issue [From 7.0.1 to 7.0.2-0: Error reading simulation model](https://forum.kicad.info/t/from-7-0-1-to-7-0-2-0-error-reading-simulation-model/41837). **It’s a bug in 7.0.2 that will be fixed in 7.0.3.**


### FreeCAD
[![FreeCAD](https://img.shields.io/static/v1?label=FreeCAD&message=0.20.29177%20(Git)&color=FC1107&logo=freecad)](https://www.freecad.org/)

FreeCAD is a general-purpose parametric 3D computer-aided design (CAD) modeler and a building information modeling (BIM) software application with finite element method (FEM) support. It is intended for mechanical engineering product design but also expands to a wider range of uses around engineering, such as architecture or electrical engineering. FreeCAD is free and open-source, under the LGPL-2.0-or-later license, and available for Linux, macOS, and Windows operating systems. Users can extend the functionality of the software using the Python programming language.  -- [Refer to Wiki](https://en.wikipedia.org/wiki/FreeCAD)

# License & Disclaimer

If you have other ideas or suggestions, please feel free to submit an issue.

<a rel="license" href="https://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="https://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.