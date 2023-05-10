[![LM317 Supply Module](https://img.shields.io/static/v1?label=&message=LM317%20Supply%20Module&color=gray&logo=Github)](https://github.com/tw1chao/LM317SupplyModule)
[![license - CC BY-SA 4.0](https://img.shields.io/static/v1?label=license&message=CC+BY-SA+4.0&color=fcaabe)](https://creativecommons.org/licenses/by-sa/4.0/)
[![forks - LM317 Supply Module](https://img.shields.io/github/forks/tw1chao/LM317SupplyModule?style=social)](https://github.com/tw1chao/LM317SupplyModule/fork)
[![stars - LM317 Supply Module](https://img.shields.io/github/stars/tw1chao/LM317SupplyModule?style=social)](https://github.com/tw1chao/LM317SupplyModule/stargazers)

# LM317 Supply Module

Although I have a high-power power supply, it only provides a single channel of voltage. Since I require multiple voltage levels, I have decided to design an LDO supply module to regulate the voltage accordingly.
I envision the supply module to be assembled in a manner similar to Lego blocks, allowing for easy expansion and modification.

## Circuit

![](./Image/LM317%20Supply%20Module.jpg)

## PCB 2D View
Single layer PCB
![](./Image/LM317%20Supply%20Module%20PCB.jpg)

## PCB 3D View

![](./Image/LM317%20Supply%20Module%20PCB%203D.png)

### Bill Of Material

| Ref         | Qnty | Value                  | Cmp name               | Footprint                                                                   | Description                                                                                              | Vendor | DNP |
|-------------|------|------------------------|------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|--------|-----|
| C1          | 1    | 10nF/16V               | C_Small                | Capacitor_SMD:C_0603_1608Metric                                             | Unpolarized capacitor, small symbol                                                                      |        |     |
| C2          | 1    | 100u/25V               | C_Polarized_Small_US   | Capacitor_Tantalum_SMD:CP_EIA-7343-30_AVX-N                                 | Polarized capacitor, small US symbol                                                                     |        |     |
| C3          | 1    | 100nF/16V              | C_Small                | Capacitor_SMD:C_0603_1608Metric                                             | Unpolarized capacitor, small symbol                                                                      |        |     |
| C4          | 1    | 100u/25V               | C_Polarized_Small_US   | Capacitor_SMD:C_0603_1608Metric                                             | Polarized capacitor, small US symbol                                                                     |        |     |
| D1, D2      | 2    | KDZVTF16B              | D_Small                | Diode_SMD:D_SOD-123F                                                        | Diode, small symbol                                                                                      |        |     |
| D3, D4      | 2    | 1N4007                 | D_Small                | Diode_SMD:D_SMA                                                             | Diode, small symbol                                                                                      |        |     |
| D5          | 1    | LED_Green              | LED_Small              | LED_SMD:LED_1206_3216Metric                                                 | Light emitting diode, small symbol                                                                       |        |     |
| J1          | 1    | Conn_01x02             | Conn_01x02             | Connector_Phoenix_MC:PhoenixContact_MC_1,5_2-G-3.81_1x02_P3.81mm_Horizontal | Generic connector, single row, 01x02, script generated   (kicad-library-utils/schlib/autogen/connector/) |        |     |
| J2, J3      | 2    | Conn_01x02             | Conn_01x02             | Connector_Molex:Molex_KK-254_AE-6410-02A_1x02_P2.54mm_Vertical              | Generic connector, single row, 01x02, script generated   (kicad-library-utils/schlib/autogen/connector/) |        |     |
| JP1, JP2    | 2    | SolderJumper_2_Open    | SolderJumper_2_Open    | Jumper:SolderJumper-2_P1.3mm_Open_TrianglePad1.0x1.5mm                      | Solder Jumper, 2-pole, open                                                                              |        |     |
| JP3         | 1    | SolderJumper_2_Bridged | SolderJumper_2_Bridged | Jumper:SolderJumper-2_P1.3mm_Bridged_RoundedPad1.0x1.5mm                    | Solder Jumper, 2-pole, closed/bridged                                                                    |        |     |
| Q1          | 1    | [DMP4011SPSQ](https://www.diodes.com/part/view/DMP4011SPSQ/#tab-details)           | DMP3013SFV             | Supply-Module-Library:Diodes_PowerDI5060-8                                  | -12A Id, -30V Vds, P-Channel Power MOSFET, 9.5mOhm Ron, 33.7nC Qg (typ),   PowerDI3333-8                 |        |     |
| Q2          | 1    | 2N7002                 | NMOS                   | Package_TO_SOT_SMD:SOT-23                                                   | N-MOSFET transistor, drain/source/gate                                                                   |        |     |
| R1          | 1    | 100R/5%                | R_Small_US             | Resistor_SMD:R_0603_1608Metric                                              | Resistor, small US symbol                                                                                |        |     |
| R2          | 1    | 10K/5%                 | R_Small_US             | Resistor_SMD:R_0603_1608Metric                                              | Resistor, small US symbol                                                                                |        |     |
| R3, R4, R9  | 3    | 100K/5%                | R_Small_US             | Resistor_SMD:R_0603_1608Metric                                              | Resistor, small US symbol                                                                                |        |     |
| R5, R8, R10 | 3    | 1K/5%                  | R_Small_US             | Resistor_SMD:R_0603_1608Metric                                              | Resistor, small US symbol                                                                                |        |     |
| R6          | 1    | 1M/5%                  | R_Small_US             | Resistor_SMD:R_0603_1608Metric                                              | Resistor, small US symbol                                                                                |        |     |
| R7          | 1    | 120R/5%                | R_Small_US             | Resistor_SMD:R_0603_1608Metric                                              | Resistor, small US symbol                                                                                |        |     |
| RV1         | 1    | 10K                    | R_Potentiometer_Small  | Supply-Module-Library:Variable_Resistance_PV36W                             | Potentiometer                                                                                            |        |     |
| SW1         | 1    | SW_SPDT                | SW_SPDT | Supply-Module-Library:SW_DIP_5176_SPDT                                      | Switch, single pole double throw                                                                         |    [5176A](https://kinsten.com.tw/index.php?route=product/product&product_id=49621&search=壓動開關5.8×5.8mm) / [TL2203EE](https://mou.sr/3LJwoE3)    |     |
| U1          | 1    | LM317_SOT-223          | [LM317_SOT-223](https://www.ti.com/product/LM317)         | Package_TO_SOT_SMD:SOT-223-3_TabPin2                                        | 1.5A 35V Adjustable Linear Regulator, SOT-223                                                            |        |     |


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