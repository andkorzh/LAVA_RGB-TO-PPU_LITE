LAVA_RGB-TO-PPU_LITE
This project converts the existing Lava RGB board into a fully functional and self-contained FPGA PPU chip that doesn't require the original RP2С02 PPU chip. It requires removing the comparators from the board and soldering several jumpers to enable the local PPU bus.

The project contains 2 palettes, switching is carried out by pin 21 of the FPGA.

Connection diagram:

![LAVA_RGB to PPU_LITE](https://github.com/user-attachments/assets/ff29d20d-76f3-47ea-a786-a65b15078fc2)


photo of the prototype:
![IMG_4818](https://github.com/user-attachments/assets/8d4dce00-bec2-4c06-9e9d-852748fe3347)

![IMG_4822](https://github.com/user-attachments/assets/7c22a19f-ffef-465c-a6dc-4a099c446955)

Be careful not to let the FPGA inputs come into contact with the 5-volt voltage from the console.
The FPGA clock input, pin 43, should be connected to the console clock generator via a 100-ohm resistor.
The CLK pad should only be connected to the CPU R/W.
Pin 52 of the FPGA controls the U8 level shifter and is not connected to the CPU R/W pin.
The board should be connected to the console using the contacts where the PPU was soldered; I've marked them in green. If a socket for the PPU and an adapter board were soldered in, they need to be removed and the adapter re-soldered to different pins.


resources used by the FPGA

<img width="565" height="752" alt="Lava_ppu_res" src="https://github.com/user-attachments/assets/94d08307-3664-4ed7-aa24-990b8fdafd81" />

Video on YouTube: https://www.youtube.com/watch?v=mdxmFLmyeGQ



