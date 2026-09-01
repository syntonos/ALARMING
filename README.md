# ALARMING!
![PCB](/Assets/3D_top.png)
![CAD](/Assets/CAD_top.png)
A small vibrating alarm that only turns off when you get up and hunt down another ESP32 button. For extra fun, you can ask your friends to hide it for you :) 

**Find the button to turn it off!**

## About
I am mildly bad at waking up in the mornings, and I think part of it is that I can just hit snooze on my alarm in bed. This is a way of circumventing that without making enough sound to annoy everyone living with me. Fun for if you have roommates!

## Assembly Instructions
### MAIN
Solder down the:
- 4x Seven-segment displays.
    - Solder one by one. Place into the throughhole slots on the top half of the PCB, making sure the decimal dot is in the bottom right corner. 
    ![alt text](/Assets/seven_seg.png)
- 1x Seeed Xiao ESP32-C3
    - SOLDER BEFORE THE OLED DISPLAY. Place header pins with the short side for the Seeed, solder the Xiao to the header pins, then solder the Xiao to the PCB. Cut off excess on the pins. 
    ![alt text](/Assets/esp32.png)
- 1x Vibrating Motor
    - SOLDER BEFORE THE OLED DISPLAY.
    - Align the two sides of the + - terminals, then solder exposed ends of the wire. 
    ![alt text](image-2.png)
- 2x Boot/EN buttons
    - SOLDER BEFORE THE OLED DISPLAY. 
    - SOLDER BEFORE LED. 
    - Align the button with the correct pads (make sure orientation is correct and the component is within the silkscreen). 
    ![alt text](image-3.png)
- 1x LED
    - SOLDER BEFORE THE OLED DISPLAY.
    - Align the direction of the LED as indicated on the silkscreen, then solder throughhole pins.
    ![alt text](image-4.png)
- 1x OLED display.
    - SOLDER AFTER ALL PARTS ABOVE. Place a header pin between the OLED display module and the PCB, with the shorter pins facing upwards, then align the display with the silkscreen outline and solder throughhole pins.
    
        ![alt text](image-5.png)
- 1x Rotary Encoder EC11
    - Place though mounting holes, then solder throughhole pins. 
    ![alt text](image-6.png)

3D-printed Case: 
- Print out the case! Take out any support struts if you have any. Insert heatsinks (4x M2 5mm for top, 4x M2 10mm for bottom half) Place the top half, making sure the port cutout is where the USB-C port is, then place the bottom half, aligning the port in the same way. Screw down the housing (4x M2 14mm Screws).

### Button
Use a keyboard switch, then solder one pin to GND on a Seeed Xiao ESP32, and another to D0. 
![alt text](image.png)
Make a case at your discretion!

## Firmware
Firmware written in Arduino IDE. Flash by copying code into Arduino IDE, then flashing the corresponding Seeed Xiao ESP32-C3 MCUs (main and button respectively).

## PCB 
### 3D Models
![3D Top](/Assets/3D_top.png)
![3D Bottom](/Assets/3D_bottom.png)
### Schematic
![Schematic](/Assets/schematic.png)
### PCB Layout
![PCB Layer 1](/Assets/pcb_layer_1.png)
![PCB Layer 2](/Assets/pcb_layer_2.png)
![PCB Layer 3](/Assets/pcb_layer_3.png)
![PCB Layer 4](/Assets/pcb_layer_4.png)

## CAD
![CAD Top](/Assets/CAD_top.png)
![CAD Bottom](/Assets/CAD_bottom.png)

## BOM
- 1x PCB (back side PCBA)
- 2x Seeed Xiao ESP32-C3
- 4x Seven-segment Display 
- 1x Rotary Encoder EC11
- 2x 4x4mm Push Switch
- 1x 3mm LED
- 1x OLED Display
- 1x Vibrating Motor

## BOM (Expanded)
- 1x PCB (back side PCBA)
- 2x Seeed Xiao ESP32-C3
- 4x Seven-segment Display 
- 1x Rotary Encoder EC11
- 2x 4x4mm Push Switch
- 1x 3mm LED
- 1x OLED Display
- 1x Vibrating Motor