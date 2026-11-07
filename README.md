# GamePad
GamePad is a handheld gamepad built built for the BBC microbit V2, The idea is really simple - plouge and play, just plough the microbit into the GamePad through the edge connector of the gameopad, and the GamePad have buttons 7 of them 4 buttons are on left side for movement UP , LEFT, RIGHT, DOWN and 3 buttons on right Menu, A, and B. It also includes a 1.8" colour TFT display, and a rechargeable 18650 battery with USB-C charging and protection, so it can be used without a cable.

<img width="1148" height="701" alt="image" src="https://github.com/user-attachments/assets/fe59d858-b928-4aeb-b395-bb5d0b73168a" />
GamePad Render

## What is it

I wanted to make an offline gamepad for myself but never tried for some reason most DIY gamepads I saw were built on an ESP or a Raspberry Pi then I came across the microbit and thought, why not make a gamepad for it. It is inspired by the Game Boy Micro, but the design and the function are a bit different.
Most microbit gamepads don't have a display, so I added one. The idea is simple flash a game onto the microbit, plug it into the edge connector on the gamepad, and play. The microbit already has a speaker on it, so I didn't add a buzzer.
<img width="572" height="507" alt="image" src="https://github.com/user-attachments/assets/3ba45015-8c0b-4728-a190-5d9bff3f9699" />

## Working

The microbit sits in an edge connector on the top side of the GamePad PCB.
<img width="1302" height="747" alt="image" src="https://github.com/user-attachments/assets/e1bdaf81-7dee-486a-95fa-c2825d05711a" />

This GamePade have
7 buttons: 4 for direction (up, down, left, right) and 3 extra function buttons like menu or mute, their function changes from game to game like they are game dependend
Display: a 1.8" ST7735 TFT display like obvoulsy we need a display for gamepad also i couldent find any footprint or 3D model for the version i am using so all of my renders are without display
LEDs on the back: controlled by a slider switch. The slider connects the board's 3V3 to the LED 3V3 line that powers all of them this is just for fun no functional use to be honest
Battery indicator: a voltage divider reads the battery level and sends it to the microbit, which decides if the battery is low. A small LED glows when it is and Also have Charging and charged indicators
Power slider: decides whether BAT+ reaches the LDO. No input to the LDO means no 3V3, and no 3V3 means no LEDs, no display and no microbit, so the whole board is off.

<img width="137" height="150" alt="image" src="https://github.com/user-attachments/assets/7a745ecf-da8f-46dc-96cb-825dc34e2327" />

## Schematics & Circuitry

This PCB was designed in KiCad, as it is free
<img width="1195" height="850" alt="image" src="https://github.com/user-attachments/assets/2f4c748d-98c8-4dbc-bbd1-20662774631f" />
I couldn't find a footprint for the display, so I used a 1x08 male header for it

## Routing
<img width="1280" height="686" alt="image" src="https://github.com/user-attachments/assets/74d17ce9-2fb4-440d-b2cd-7ffbdadd2742" />
<img width="1303" height="730" alt="image" src="https://github.com/user-attachments/assets/aad79841-d608-4c05-a272-8dfa9ef777ce" />
I poured copper with the GND net on both the top and bottom layers, and added vias to connect the two layers. I also added M3 holes for mounting

## 3D view
<img width="1431" height="875" alt="image" src="https://github.com/user-attachments/assets/da295556-e827-40ae-b16b-19261e9640b0" />
PCB with 3D models, exported as .step so I could design the case around it

## Case

For the case I went with two transparent acrylic panels, one on top and one on bottom. The PCB sits between them, held by hex spacers. I also made button extenders, which can be 3D printed.

<img width="1407" height="677" alt="Screenshot 2026-10-29 111659" src="https://github.com/user-attachments/assets/29a02c67-3e22-42bb-9a4a-1e6884fd5915" />
<img width="1093" height="588" alt="Screenshot 2026-10-29 111716" src="https://github.com/user-attachments/assets/585340e0-84e1-4ebf-bb2c-87820f792583" />
Top plate

<img width="1296" height="705" alt="Screenshot 2026-10-29 111742" src="https://github.com/user-attachments/assets/355adf2e-fb81-493e-a3b0-7a179f18263c" />
Bottom plate

<img width="1192" height="687" alt="Screenshot 2026-10-29 111807" src="https://github.com/user-attachments/assets/04baa58e-b94b-42cc-8288-01574fbadda7" />
Both panels together

<img width="1295" height="802" alt="Screenshot 2026-10-29 111902" src="https://github.com/user-attachments/assets/ee39c212-07d4-4475-bf5b-8fb32b536da7" />
Final GamePad
