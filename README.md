LAVA_RGB-TO-PPU_LITE
This project converts the existing Lava RGB board into a fully functional and self-contained FPGA PPU chip that doesn't require the original RP2С02 PPU chip. It requires removing the comparators from the board and soldering several jumpers to enable the local PPU bus.

The project contains 2 palettes, switching is carried out by pin 21 of the FPGA.

Connection diagram:
<img width="1095" height="588" alt="LAVA_RGB to PPU_LITE" src="https://github.com/user-attachments/assets/986653a5-c913-40b8-97a9-cacb0d49651b" />

photo of the prototype:
![IMG_4818](https://github.com/user-attachments/assets/8d4dce00-bec2-4c06-9e9d-852748fe3347)

resources used by the FPGA

<img width="565" height="752" alt="Lava_ppu_res" src="https://github.com/user-attachments/assets/94d08307-3664-4ed7-aa24-990b8fdafd81" />

Video on YouTube: https://www.youtube.com/watch?v=mdxmFLmyeGQ



