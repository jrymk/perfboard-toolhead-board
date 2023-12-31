# perfboard-toolhead-board
An RP2040 powered toolhead board, not intended to replace the cable chains, but to simplify wiring and add expandability

## Pinout

| peripheral | hardwire | rp2040 |
| --- | --- | --- |
| hotend | 24V, **HE0** | |
| hotend thermistor | GND | IO26 |
| stepper | 24V | IOx, IOx, IOx, IOx, IOx |
| rp2040 | GND, 5V, **TX, RX** | IO0, IO1 |
| hotend fan | 24V | IOx |
| parts cooling fan | 24V | IOx |
| rgb | GND. 5V | IOx |
| probe | GND, 24V, **PROBE** | |
| endstops | GND, **ENDSTOP-X, ENDSTOP-A** | 3V3, IOx, IOx... |
| adxl345 | GND | 3V3, SPI0 |
| thermistors | GND | IO27, IO28, IO29 |

Connections to the electronics bay
- J1 (XH2.54-4P)
  - HE
  - GND
  - 5V
  - 24V
- J2 (XH2.54-5P)
  - RP-TX
  - RP-RX
  - ENDSTOP-1
  - ENDSTOP-2
  - PROBE
 
## Why

Compared to a CAN toolhead board...
- simple breakout of the uart pins, instead of CAN which I don't really like
- hardwired probe and endstop signal to prevent multi mcu homing causing inaccuracies, can probe faster
- DIYable with cheap and easily obtainable parts, also customizable
- all XH2.54 connectors, very common in 3D printers and you should have an assortment kit of it
- remote ADXL that hard mounts nearer the nozzle for actually useful readings (the shaper results of EBB36 mounted on the extruder on my Voron 0 is barely usable)

Compared to hartk's Stealthburner Toolhead Board...
- from 16 wires to 9 wires
- from hard to find molex (14p/2p input and 2p heater/thermistor) to super common XH2.54 (rated for 3A peak, so up to 72W heater)
- from PH2.0 to XH2.54 (for fans, probe and other peripherals)
- tons of pins for expandability, like filament, ERCF/TradRack sensors, load cells, etc.


## BOM
![IMG_1769](https://github.com/jrymk/protoboard-toolhead-board/assets/39593345/c42bd70b-a8af-4665-95f9-85ee6975bfc9)

- 2.54 perfboard
- Waveshare RP2040-Zero
- A kit of JST XH2.54 connectors (from 2p to 5p and 6p, which is pretty common for the kits)
- A kit of SMD transistors, or specifically, AO3400 mosfets and BAV99 diodes
- A kit of SMD resistors
- Maybe some 2.54 headers and jumpers
- Wrapping wire and solder, and a soldering iron...

## Instructions
Not yet. Not even I have started. But it's exciting right? Right?
