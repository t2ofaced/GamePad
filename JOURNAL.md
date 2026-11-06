---
title: "Microbit Gamepad"
author: "t2ofaced"
description: "A gamepad for the microbit with a display"
created_at: "2026-09-12"
---

# 06 Nov 2026: Game for Microbit GamePad

![image](https://twisted.hackclub-assets.com/3c4c66dc-9b00-4b4f-b6e2-43749515a694-188839/image.png)
well this was kinda hard for me but it is working well

AND

![image](https://twisted.hackclub-assets.com/4677cc6e-cd65-4515-bf0c-6dcab064ef31-20938/image.png)
EVIL DUCKYY

**Total time spent: 1 hour 36 minutes**

# 29 Oct 2026: Case design

So i was thinking about case for this gamepad and this is what i thought - 2 transparent acrylic panels one for top and one for bottom

![image](https://twisted.hackclub-assets.com/04364791-76b6-4952-977d-ad1e01b6e6c9-218496/image.png)

![image](https://twisted.hackclub-assets.com/a8354f83-7838-4c9d-a3ab-c148ea7b4ce7-295225/image.png)
Top plate of the gamepad

![Screenshot 2026-10-29 111742](https://twisted.hackclub-assets.com/fea9dd63-5296-4126-a30f-070ce518633b-132723/screenshot-2026-10-29-111742.png)
bottom plate of the gamepad

![Screenshot 2026-10-29 111807](https://twisted.hackclub-assets.com/3165884d-ed56-4bdf-a796-6858fb697822-237501/screenshot-2026-10-29-111807.png)

![Screenshot 2026-10-29 111834](https://twisted.hackclub-assets.com/9ae872ec-ad55-4361-97bf-a9bd0d9d387d-191486/screenshot-2026-10-29-111834.png)
top and bottom panels and together

![Screenshot 2026-10-29 111816](https://twisted.hackclub-assets.com/e5c409c1-d771-4c46-b61d-bf8a40a2fb5d-20789/screenshot-2026-10-29-111816.png)
these black cylinders are Hex spacers and the pcb is between them

![Screenshot 2026-10-29 111902](https://twisted.hackclub-assets.com/39a2ec5b-7e0a-43e8-8e8f-a7e5145ef847-570679/screenshot-2026-10-29-111902.png)
final view also made these button extenders these are also 3d printable

**Total time spent: 1 hour 8 minutes**

# 11 Oct 2026: Schematic completed, placement and routing

![image](https://twisted.hackclub-assets.com/598e9452-8f80-499f-b317-87a9396f5fb1-74059/image.png)
completed schematic and then assigned footprint to the components. I was unable to find the footprint of display so i used a 1X08 male header

After that component placement

![image](https://twisted.hackclub-assets.com/fffc2919-2eb3-44dd-9508-f229bc609451-314166/image.png)

![image](https://twisted.hackclub-assets.com/b6873511-e6e2-48e5-9c84-a8bfb6fc84fb-88131/image.png)
and i used the wrong footprint

![image](https://twisted.hackclub-assets.com/b7f30e06-1486-49a8-b973-d751463c9b3a-33894/image.png)
this is new one

ig they look the same here difference is in schematic

![image](https://twisted.hackclub-assets.com/6ac85577-dcd5-43fd-9944-80d407fa9495-33567/image.png)
old

![image](https://twisted.hackclub-assets.com/551dc707-c73e-4401-9ce2-e2528b8afe56-36107/image.png)
New

![image](https://twisted.hackclub-assets.com/70cd6ec1-f55d-49ba-9dfb-2c605675395d-181126/image.png)

then started routing

![image](https://twisted.hackclub-assets.com/dff364fa-cc13-4721-80e0-ec24b328a633-169663/image.png)
final routing and component placement

![image](https://twisted.hackclub-assets.com/a53d0d14-363d-49e9-856a-f4e1daec9825-203660/image.png)
poured cu with net label gnd on both top and bottom layer added vias to connect these two layers and added m3 holes

![image](https://twisted.hackclub-assets.com/195aba6c-a7be-48bf-a352-fbb98b956d55-222743/image.png)
added 3d files of components and exported .step file so that i can make case around it

**Total time spent: 9 hours 14 minutes**

# 29 Sep 2026: LDO, power slider and battery circuit

![image](https://twisted.hackclub-assets.com/ba166d63-5a07-401c-9d09-d989eddf53fe-23342/image.png)
wired SPX3819M5-L-3-3/TR LDO , bored with ams117 so tried this new ldo and its max op is 500 mA this should work in theory
also added a slider to turn on and off the game pad like it decides whether bat+ goes to ldo or not and u can guess pretty much no input to ldo means no 3v3 and no 3v3 means no led lcd and microbit so board will be off

![image](https://twisted.hackclub-assets.com/b3c6e7db-5fd2-47ed-af99-3234a207b58e-20020/image.png)
i add this small circuit left side is a voltage divider which senses the battery voltage level and sends this to a microbit which decides if its low or not and right part is led which glows if battery is low

![image](https://twisted.hackclub-assets.com/c3af9a02-dc2a-47a7-8ed6-00c4abbb621d-19097/image.png)
and these are the led on the back side which will be controlled by a slider this slider connects the 3v3 of board to led 3v3 which connects all the leds

and completed display connections

![image](https://twisted.hackclub-assets.com/180f5342-8d3f-4eb9-840c-47a8ffe98461-19088/image.png)

**Total time spent: 1 hour 29 minutes**

# 12 Sep 2026: Component search and schematic

idk but i am not able to enter log hours anyway

SO i started with component searched finalized some like

![image](https://twisted.hackclub-assets.com/33bda553-43cf-499a-a10e-ebd96fe05ebc-174982/image.png)
perfectly sized and price is also fair good for me

and started schematic i am doing this on kicad as its free

i wired display and type c

![image](https://twisted.hackclub-assets.com/a394c47f-5898-472e-a7ed-7029bf4746cc-26041/image.png)

![image](https://twisted.hackclub-assets.com/90d26b54-8bff-40d9-8f92-b2db37c2f88b-15970/image.png)

in this ses i wired microbit edge connector , also it took me a lot of time to just find right edge connector footprint

![image](https://twisted.hackclub-assets.com/a24b7d99-ae60-4303-9430-a148cc3d2b2c-25295/image.png)

and here are the 7 btns of gamepad like 4 for direction up down right left and other 3 are extra function like menu and other function mute maybe not decided yet like they function different with different games type

![image](https://twisted.hackclub-assets.com/253139de-3e82-4981-ba82-41806fe7adc9-11973/image.png)

and this is typical 1 cell charging ic nothing special

![image](https://twisted.hackclub-assets.com/4de87a9b-8c04-4765-a3b0-fdfc87eb9e33-15737/image.png)

protection circuit again standard dw01a ic with fs805, ngl i was confused here these protection circuits are simple but confusing at the same time

![image](https://twisted.hackclub-assets.com/a9758f46-1c0b-444c-8f4f-6b0625e2ffa7-13730/image.png)

**Total time spent: 2 hours 7 minutes**

# 15 Sep 2026: The idea (not on hacktime)

so I wanted to make a offline gamepad for myself from a long time but I never tried for some reason like most diy gamepad I saw were using esp and rpis but today recently i saw something interesting a microbit so now i wanna make a gamepad for microbit and this is inspired by this Gameboy micro but my gamepad gonna be little different in design as well as function

![image](https://twisted.hackclub-assets.com/241e5842-116e-4a27-ad5a-837395870ac0-166641/image.png)

this is close to my imagination my microbit will also mount this on type of edge connector on top side

![image](https://twisted.hackclub-assets.com/a3442e95-22fd-4550-af7d-a07325c161bc-388278/image.png)

this is what I am thinking

![image](https://twisted.hackclub-assets.com/0c647b0d-86a8-4ecb-9f0c-f5784562ba50-98238/image.png)
as u saw I added a display too and I think microbit already have buzzer in it so I don't need that

and yeah most of the microbit gamepads don't include any display

![image](https://twisted.hackclub-assets.com/546db954-8f25-4ef8-83d0-361732fcd8f2-358871/image.png)

i like this idea because i can flash games in microbit easily then connect it to edge connector of gamepad and enjoy

and i am gonna use 3.7 v bat for power thats it for now ig

**Total time spent: 1 hour**
