LAVA_RGB-TO-PPU_LITE
This project converts the existing Lava RGB board into a fully functional and self-contained FPGA PPU chip that doesn't require the original RP2С02 PPU chip. It requires removing the comparators from the board and soldering several jumpers to enable the local PPU bus.

The project contains 8 palettes. Palette switching with a button. The button is connected to DATA pad.

000 - Composite Direct;

001 - Nintendulator NTSC;

010 - FBX Magnum;

011 - Sony CXA;

100 - PC-10

101 - Wavebeam

110 - PAL

111 - Kitrinx (USA)


Regions are switched by pins 32 and 29 of the FPGA.

Connection diagram:

<img width="1593" height="865" alt="LAVA_RGB to PPU_LITE" src="https://github.com/user-attachments/assets/6e0afe45-bb7b-4efa-941e-d0c566f020cd" />


The green color on the diagram indicates the connection points to the console board.

photo of the prototype:
![IMG_4843](https://github.com/user-attachments/assets/bc8f961f-735e-4d01-8591-6c2b00f9580f)


![IMG_4822](https://github.com/user-attachments/assets/7c22a19f-ffef-465c-a6dc-4a099c446955)

Be careful not to let the FPGA inputs come into contact with the 5-volt voltage from the console.
The FPGA clock input, pin 43, should be connected to the console clock generator via a 100-ohm resistor.
The CLK pad should only be connected to the CPU R/W.
Pin 52 of the FPGA controls the U8 level shifter and is not connected to the CPU R/W pin.
The board should be connected to the console using the contacts where the PPU was soldered; I've marked them in green. If a socket for the PPU and an adapter board were soldered in, they need to be removed and the adapter re-soldered to different pins.


resources used by the FPGA

<img width="575" height="748" alt="Lava_ppu_res" src="https://github.com/user-attachments/assets/2f53591c-9bca-496b-afcb-03c6c1239f8d" />


Video on YouTube: https://www.youtube.com/watch?v=mdxmFLmyeGQ

Added additional composite output.

<img width="3120" height="2560" alt="composit_DAC" src="https://github.com/user-attachments/assets/4777b933-6c25-49ea-99d3-5c21b80d1f31" />

COMPOSIT[6:0]   24, 21, 20, 19, 18, 17, 16  pin FPGA 



