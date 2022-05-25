#  MikroLeo
## 4-bit Didactic Microcomputer

<!-- This is a comment -->

The project is in the final testing stage.  
This project was developed mainly for educational purposes.  
It is a fully open-source hardware and software project.  
Soon, the project files will be here!

Main Features:
- 2k x 16 ROM (up to 4k)
- 2k x 4 RAM (up to 4k)
- 4 Output Ports (16 outputs)
- 4 Input Ports (16 inputs)
- single cycle Instruction/RISC
- Harvard Architecture
- 3 execution modes:
   * step
   * 3MHz (precise time)
   * adjustable clock speed
- no MPU/MCU or complex chips
- no microcode
- Built with 74HCTxxx integrated circuits
- Dual layer Single board with 295.9mm x 196.9mm

# MikroLeo Architecture  
<img src="https://user-images.githubusercontent.com/60040866/169953214-34b667ca-379c-4391-9c50-69db36c3133b.png" width="85%" height="85%">

# Intruction Set  

<img src="https://user-images.githubusercontent.com/60040866/167204731-90cd0c0e-c29a-49bc-8cfe-85326740a78d.png" width="80%" height="80%">  

# Documentation  

**MikroLeo has four Registers**  
`ACC` - Acumulator - Stores the result of logical and arithmetic operations. Moreover, ACC stores data that is read from or written to RAM.  
`RA` - General purpose Register (also used for addressing).  
`RB` - General purpose Register (also used for addressing).  
`RC` - Special purpose Register used for addressing.  

**Two Flags**  
Flags are bits accessible only by conditional jump Instructions (JPC and JPZ).  

`CF` - Carry Flag - It is Set (CF=1) by ADD Instruction if it produces a carry or by SUB/CMP instruction if it results in a borrow.  
`ZF` - Zero Flag - It is affected by all operations that change the contents of ACC. It is Set (ZF=1) if the result of the last operation was zero.    

**Addressing Modes**  

<ins> *Immediate* </ins>  

In immediate addressing, the operand (n) is located after the opcode, being part of the Instruction itself.  

Example:  
LDI ACC,1  
LDI ACC,0xA  
NAND ACC,0  
OUTA 0xF  
CMP ACC,0  
SUB ACC,1  
ADD ACC,5  


...

-------------------------------------------------
# Pictures
Breadboard:  
<img src="https://user-images.githubusercontent.com/60040866/166626556-bd559537-f371-4d85-87b8-ae23018d6fd7.jpg" width="40%" height="40%">  

PCB (Kicad 3D viewer):  
<img src="https://user-images.githubusercontent.com/60040866/166627152-4c3770eb-8091-40ed-be2d-034289695b60.png" width="60%" height="60%">  

PCB Prototype:  
<img src="https://user-images.githubusercontent.com/60040866/166628285-47b3ee24-fd4e-49f8-9bca-21af1cec307d.jpg" width="55%" height="55%">  

-------------------------------------------

# Development stages

- [x] - Bibliographic research
- [x] - Architecture definition
- [x] - Circuit design
- [x] - Circuit simulation
- [x] - Prototype assembly on breadboard
- [x] - Printed circuit board design
- [x] - Prototype assembly on PCB
- [ ] - Final tests


# History and Motivation
Since the time I took an 8086 assembly language programming course, this project has been something that I have always wanted to do.  
Some sources of inspiration can be seen at:  

http://www.sinaptec.alomar.com.ar/2018/03/computadora-de-4-bits-capitulo-1.html  
https://www.bigmessowires.com/nibbler/  
https://gigatron.io/  
https://eater.net/  
https://apollo181.wixsite.com/apollo181/specification  

# Dedication
This project is dedicated to my son, Leonardo Pimentel Acordi  

# Acknowledgements  

The authors would like to thank the IFPR (Instituto Federal do Paraná) and CNPq (Conselho Nacional de Desenvolvimento Científico e Tecnológico) for partially funding this project.

# Authors  

>Edson Junior Acordi  
Matheus Fernando Tasso  
Carlos Daniel de Souza Nunes  

# License

**Hardware:** Licensed under CERN-OHL-S v2 or any later version  
https://ohwr.org/cern_ohl_s_v2.txt

**Software:** Licensed under GNU GPL v3  
https://www.gnu.org/licenses/gpl-3.0.txt

**Documentation:** Licensed under CC BY-SA 4.0  
https://creativecommons.org/licenses/by-sa/4.0/
