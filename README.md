# GamePad

GamePad is a handheld gamepad built for the BBC microbit V2 the idea is really simple - plug and play, just plug the microbit into the GamePad through the edge connector of the gamepad and playy, the GamePad have 7 buttons and 4 of buttons are on left side for movement UP , LEFT, RIGHT, DOWN and 3 buttons on right Menu, A, and B it also includes a 1.8" colour TFT display, and a rechargeable 18650 battery with USB-C charging and protection, so it can be used without a cable.

<p align="center">
  <img src="https://github.com/user-attachments/assets/fe59d858-b928-4aeb-b395-bb5d0b73168a" width="700" alt="GamePad Render"><br>
  <em>Figure 1: GamePad Render</em>
</p>

## What is it

I wanted to make an offline gamepad for myself but never tried for some reason most DIY gamepads i saw most of the game consoles were built on an ESP or a raspberry pi and later i came across the microbit and thought why not make a gamepad for it it is inspired by the Game Boy Micro but the design and the function are a diffrent 

Most microbit gamepads don't have a display so i added one the idea is simple flash a game onto the microbit, plug it into the edge connector on the gamepad and play the microbit already has a speaker on it, so i didn't add a buzzer

<p align="center">
  <img src="https://github.com/user-attachments/assets/3ba45015-8c0b-4728-a190-5d9bff3f9699" width="500" alt="Figure 2"><br>
  <em>Figure 2</em>
</p>

## Working

The microbit sits in an edge connector on the top side of the GamePad PCB

<p align="center">
  <img src="https://github.com/user-attachments/assets/e1bdaf81-7dee-486a-95fa-c2825d05711a" width="700" alt="Figure 3"><br>
  <em>Figure 3</em>
</p>

This GamePad have

- **7 buttons:** 4 for direction (up, down, left, right) and 3 extra function buttons like menu or mute, their function changes from game to game like they are game dependent
- **Display:** a 1.8" ST7735 TFT display like obviously we need a display for gamepad also i couldn't find any footprint or 3D model for the display version i am using so all of my renders are without display
- **LEDs on the back:** controlled by a slider switch. The slider connects the board's 3V3 to the LED 3V3 line that powers all of them this is just for fun no functional use to be honest
- **Battery indicator:** a voltage divider reads the battery level and sends it to the microbit, which decides if the battery is low this also have Charging and charged indicators
- **Power slider:** decides whether BAT+ reaches the LDO no input to the LDO means no 3V3, and no 3V3 means no LEDs, no display and no microbit, so the whole board is off.

<p align="center">
  <img src="https://github.com/user-attachments/assets/7a745ecf-da8f-46dc-96cb-825dc34e2327" width="137" alt="Figure 4"><br>
  <em>Figure 4</em>
</p>

## Schematics & Circuitry

This PCB was designed in KiCad, as it is free

<p align="center">
  <img src="https://github.com/user-attachments/assets/2f4c748d-98c8-4dbc-bbd1-20662774631f" width="800" alt="Schematic"><br>
  <em>Figure 5: Schematic</em>
</p>

I couldn't find a footprint for the display so i used a 1x08 male header for it

## Routing

<p align="center">
  <img src="https://github.com/user-attachments/assets/74d17ce9-2fb4-440d-b2cd-7ffbdadd2742" width="700" alt="Routing"><br>
  <em>Figure 6: Routing</em>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/aad79841-d608-4c05-a272-8dfa9ef777ce" width="700" alt="Routing"><br>
  <em>Figure 7: Routing</em>
</p>

I poured copper with the GND net on both the top and bottom layers, and added vias to connect the two layers i also added M3 holes for mounting

## 3D view

<p align="center">
  <img src="https://github.com/user-attachments/assets/da295556-e827-40ae-b16b-19261e9640b0" width="700" alt="3D view"><br>
  <em>Figure 8: PCB with 3D models, exported as .step so I could design the case around it</em>
</p>

## Case / CAD

The Case/CAD is designed in Onshape

**Onshape:** [Open CAD model](https://cad.onshape.com/documents/08b3f6e79f648ac5b1a837d6/w/fd33090a4ac3aeb19b806cc8/e/8d36c46b3c2b914df7cd311f)

For the case i went with two transparent acrylic panels, one on top and one on bottom the PCB sits between them, held by hex spacers i also made button extenders which can be 3D printed.

<p align="center">
  <img src="https://github.com/user-attachments/assets/29a02c67-3e22-42bb-9a4a-1e6884fd5915" width="700" alt="Top plate"><br>
  <em>Figure 9: Top plate</em>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/585340e0-84e1-4ebf-bb2c-87820f792583" width="700" alt="Top plate"><br>
  <em>Figure 10: Top plate</em>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/355adf2e-fb81-493e-a3b0-7a179f18263c" width="700" alt="Bottom plate"><br>
  <em>Figure 11: Bottom plate</em>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/04baa58e-b94b-42cc-8288-01574fbadda7" width="700" alt="Both panels together"><br>
  <em>Figure 12: Both panels together</em>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/ee39c212-07d4-4475-bf5b-8fb32b536da7" width="700" alt="Final GamePad"><br>
  <em>Figure 13: Final GamePad</em>
</p>

## Bill of Materials

| Part Name | Quantity | Link | Info | Price (USD) |
|-----------|:--------:|------|------|------------:|
| JLCPCB PCB Manufacturing & Shipping | 5 | [Link](https://jlcpcb.com/) | PCB | $17.75 |
| Micro:bit Edge Connector 40-pin 90 Degree | 1 | [Link](https://www.flipkart.com/yellow-tommy-microbit-40-pin-header-90-degree-angle-edge-connector-pack-5-electronic-components-hobby-kit/p/itm9f87dd64a093b) | Microbit Edge Connector | $7.43 |
| BBC Microbit V2 | 1 | [Link](https://robu.in/product/bbc-micro-bit-v2-pocket-sized-single-board-computer/) | MCU | $22.85 |
| 18650 SMD Single Battery Holder | 1 | [Link](https://robu.in/product/18650-battery-holder-smd-smt/) | 18650 Battery Holder | $0.5 |
| TP4056 SMD IC | 1 | [Link](https://robu.in/product/1-month-warranty-1253/) | Li-ion Charger IC | $0.1 |
| DW01A Battery Protection IC SOT-23-6 | 3 | [Link](https://robu.in/product/dw01a-4-3v-lithium-ion-lithium-polymer-battery-protection-ic-6pin-sot-23/) | Battery Protection IC | $0.13 |
| FS8205A Dual MOSFET SOT-23-6 | 2 | [Link](https://robu.in/product/1-month-warranty-398/) | Dual N-MOSFET | $0.18 |
| SPX3819M5-L-3.3 LDO SOT-23-5 | 1 | [Link](https://robu.in/product/spx3819m5-l-3-3-tr-500ma-low-noise-ldo-voltage-regulator-5-pin-sot-23/) | 3.3V LDO Regulator | $0.24 |
| AO3400A MOSFET SOT-23 | 1 | [Link](https://robu.in/product/1-month-warranty-414/) | N-MOSFET | $0.11 |
| SMF30A TVS Diode SOD-123FL | 10 | [Link](https://robu.in/product/smf30a-slkor-4-1a-48-4v-33-3v-30v-sod-123fl-esd-and-surge-protection-tvs-esd-rohs/) | TVS Diode | $0.1 |
| USB Type-C 16-Pin Female SMD | 1 | [Link](https://robu.in/product/type-c-31-m-16-hroparts-1-6p-female-type-c-smd-usb/) | USB-C Port | $0.4 |
| 1.8 inch SPI TFT 128x160 ST7735 Display | 1 | [Link](https://robu.in/product/62060/) | TFT Display | $3.29 |
| Tactile Push Button 6x6x4.3mm | 7 | [Link](https://robu.in/product/6x6x8mm-tactile-push-button-switch-pack-of-20/) | Tactile Switches | $0.15 |
| Slide Switch 3-Pin SPDT 2.54mm | 7 | [Link](https://robu.in/product/1-month-warranty-255/) | SPDT Slide Switch | $0.13 |
| 0805 SMD LED | 7 | [Link](https://robu.in/product/0805-surface-mount-led-green-50-pcs/) | SMD LED | $0.1 |
| 100nF 0805 SMD Capacitor | 14 | [Link](https://robu.in/product/100nf-0805-surface-mount-multilayer-ceramic-capacitor-pack-of-40/) | 100nF Capacitor | $0.13 |
| 10uF 0805 SMD Capacitor | 6 | [Link](https://robu.in/product/10uf-10000nf-25-v-capacitor-0805-smd-package-pack-of-10/) | 10uF Capacitor | $0.20 |
| 100 Ohm 0805 Resistor | 1 | [Link](https://robu.in/product/100-ohm-1-4w-0805-surface-mount-chip-resistor-10-pcs/) | Resistor | $0.11 |
| 470 Ohm 0805 Resistor | 5 | [Link](https://robu.in/product/rc0805jr-07470kl-yageo-smd-chip-resistor-470-kohm-%C2%B1-5-125-mw-0805-2012-metric-thick-film-general-purpose/) | Resistor | $0.1 |
| 1K 0805 Resistor | 4 | [Link](https://robu.in/product/1k-ohm-1-4w-0805-surface-mount-chip-resistor-pack-of-10/) | Resistor | $0.1 |
| 1.2K 0805 Resistor | 1 | [Link](https://robu.in/product/rc0805fr-071k2l-yageo-smd-chip-resistor-1-2-kohm-%C2%B1-1-125-mw-0805-2012-metric-thick-film-general-purpose/) | Resistor | $0.1 |
| 5.1K 0805 Resistor | 2 | [Link](https://robu.in/product/ac0805fr-075k1l-yageo-res-thick-film-0805-5-1k-ohm-1-0-125w1-8w-%C2%B1100ppm-c-pad-smd-t-r-automotive-aec-q200/) | Resistor | $0.1 |
| 10K 0805 Resistor | 2 | [Link](https://robu.in/product/rc0805jr-0710kl-yageo-res-thick-film-0805-10k-ohm-5-0-125w1-8w-%C2%B1100ppm-c-pad-smd-t-r/) | Resistor | $0.1 |
| 120K 0805 Resistor | 1 | [Link](https://robu.in/product/rc0805fr-07120kl-yageo-res-thick-film-0805-120k-ohm-1-0-125w1-8w-%C2%B1100ppm-c-pad-smd-t-r/) | Resistor | $0.1 |
| 300K 0805 Resistor | 1 | [Link](https://robu.in/product/rc0805fr-07300kl-yageo-res-thick-film-0805-300k-ohm-1-0-125w1-8w-%25c2%25b1100ppm-c-pad-smd-t-r/) | Resistor | $0.1 |
| **TOTAL** | | | | **~ $61.81** |
