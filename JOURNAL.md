title: Pencilgraver
author: darsh gupta
description: a handheld laser designed to draw on paper via burning
created: june 25th, 2025

## day 1: research
june 25th

first steps:
 - requirements
 - bill of materials
 - cool features i could add on top of regular lasers

initial requirements:
 - capable of coloring paper through burns moderately quickly
 - accurate enough to sketch designs without frustration
 - light enough to hold in my hand to draw
 - wont randomly turn on and burn my eyes/home

how lasers work (apparently):
 - laser diode: amplifies light
 - laser driver: powers laser diode with dc constant current
 - focusable lens: tightens beam to improve burn

 suppport parts: 
 - diode housing: holds diode and lens, must be precise
 - heatsink: prevent overheating at high powers
 - full body: 3d printed handheld case
 - wiring: connect power, pcb, and driver

+1.5 hours

## day 2: research specific components
june 26th

additional features i want ideally if budget allows for it:
 - adjustable strength
 - oled display for battery and power
 - tilt shutoff
 - timeout shutoff
 - buzzer feedback
 - rechargable via usb c
 - battery protection

for my burning goals, chatgpt recommends a 2.5W 450nm diode
unforunately, those are very expensive (~$115)
upon further research, cheap diodes include a 638nm 2.5W diode and a 447nm 5W diode; i'll choose the 5W diode but this will require more cooling

diode (5W 447nm):
https://www.aliexpress.com/item/1005008369496353.html
https://www.aliexpress.com/item/1005007203647604.html
https://www.aliexpress.com/item/1005008125779029.html

https://lasertree.com/products/osram-plpt9-450lb_e-450nm-5w-blue-laser-diode
https://www.digikey.ca/en/products/detail/ams-osram-usa-inc/PLPT9-450LB-E/14552504
https://www.aliexpress.com/item/1005009103059423.html

driver (5W output): 
https://www.aliexpress.com/item/1005006993930009.html
https://www.aliexpress.com/item/1005005905789715.html

battery: https://www.aliexpress.com/item/1005008360339464.html

focus lens:
https://www.aliexpress.com/item/1005006749216766.html
https://www.aliexpress.com/item/32621541471.html

heat sink: https://www.aliexpress.com/item/1005003323689097.html

pcb stuff:

(no) MOSFET IRFZ44NPBF (bridge between driver and microcontroller): https://www.aliexpress.com/item/1005009254470339.html

(no) type c charger with protection: https://www.aliexpress.com/item/1005004427739715.html

type c 3S module IP2369: https://www.aliexpress.com/item/1005008766304319

microcontroller: https://www.aliexpress.com/item/1005002651134172.html

oled screen: https://www.aliexpress.com/item/1005008640132638.html

rotary encoders: https://www.aliexpress.com/item/1005005983134515.html

tilt sensor: https://www.aliexpress.com/item/1005003701133575.html

buzzer: https://www.aliexpress.com/item/1005006201550296.html

buttons: https://www.aliexpress.com/item/1005008024309525.html

BOM v1:
PLPT9 450LB_E 447nm 5W Blue Laser Diode 9mm - 48 (https://www.aliexpress.com/item/1005007203647604.html)
12V 40W Blue Laser Driver Board for CNC Laser Engraving Cutting Module Head PWM/TTL 5W 5500mw 6W Adapter Board - 22 (https://www.aliexpress.com/item/1005006993930009.html)
G2 Focal Lens Collimation Collimator Glass - 9 (https://www.aliexpress.com/item/1005006749216766.html)
3x 18650 3500mAh 3.7V 100% Genuine INR18650-35E Rechargeable Lithium Battery - 33 (https://www.aliexpress.com/item/1005008360339464.html)
IP2369 45W 2S 3S 4S 5S 6S Lithium Battery Charging Discharger Module Li-ion - 9 (https://www.aliexpress.com/item/1005008766304319)
STM32F103C8T6 - 1 (https://www.aliexpress.com/item/1005002651134172.html)
0.91 Inch 128x32 IIC I2C White / Blue OLED LCD Display DIY Module - 3 (https://www.aliexpress.com/item/1005008640132638.html)
360 Degree Rotary Encoder EC11 - 2 (https://www.aliexpress.com/item/1005005983134515.html)
GY-521 MPU-6050 module - 3 (https://www.aliexpress.com/item/1005003701133575.html)
Active Buzzer - 2 (https://www.aliexpress.com/item/1005006201550296.html)
Metal Push Button Switch Momentary - 4 (https://www.aliexpress.com/item/1005008024309525.html)

chatgpt says this is good so we up !!

total: $140

+3 hours

## day 3: sketch + rough cad
july 2nd/3rd

basing this off of the pine64 pinecil bc i like the design and also have one

the biggest component is the diode driver, at 40mm by 40mm which is unfortunate bc thats way too big to look like the pinecil
big pivot: am going to put everything into pcb


all parts:
![schem 1](assets\image.png)

connected some stuff
![schem 2](assets\image2.png)

+3 hours

time to fix errors
![schem 3](assets\image.png)