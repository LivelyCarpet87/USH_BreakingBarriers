# Before Apple II

## Background

Older computers had 8-bit binary memory, with addresses stored to as octal numbers. They accepted input through a series of on/off switches and gave output through an array of LED lights. To use a computer, people needed to be adept at understanding memory addresses, memorizing binary opcodes, comprehending boolean algebra (AND, OR, NOT, NAND, NOR), and translating between decimal, octal, and binary systems. 

![Boolean Logic in Altair 8800 Operator's Manual](https://raw.githubusercontent.com/LivelyCarpet87/USH_BreakingBarriers/Sites/images/LogicGates.png "Boolean Logic")

---

## Actual Usage

Before the personal computer was popularized, computers were not designed with the average person in mind. On these older computers, commands did not exist. What we think of commands like copy and paste were in reality programs composed of opcodes that had to be made. The computer interface was a panel of switches and lights that required specially formatted user input. 

![Front of Altair 8800](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b2/MITS_Altair_8800_Front_Panel.jpg/1598px-MITS_Altair_8800_Front_Panel.jpg)

### 1. Program Design

For example, the command for numerical addition (which assumes the user inputs the numbers before execution), known as "ADD" or "+", consists of the following opcodes:

1. LDA (Load the data in the address the pointer is at to RAM)

2. MOV (Move the pointer to the second address)

3. LDA (LoaD the number in current Address)

4. ADD (Adding 2 numbers stored in the two 2 addresses)

5. STA (Store result in new memory address)

### 2. Coding

According to the Altair 8800 Operator's manual, to create a such program on the computer, the user needed to:

1. reset the pointer by flicking the "RESET" switch

2. Enter ALL the opcodes manually. To enter each opcode:
   
   1. The user needed to find the binary opcode from their memory or the manual. For example, "11 000 011" represents the "JMP", or jump. 
   
   ![Opcodes](https://raw.githubusercontent.com/LivelyCarpet87/USH_BreakingBarriers/Sites/images/Intel8080Instructions.png)
   
   1. The user enters the opcode by flicking a row of 8 switches (ON for 1, OFF for 0). In continuation of the previous example, the "JMP" opcode requires the user to set the row of 8 switches to ON,ON,OFF,OFF,OFF,OFF,ON,ON. 
   
   2. The user flicks the "DEPOSIT NEXT" switch to load this command into memory. 
   
   3. If the command involves a memory address:
      
      1. the user has to translate the address from octal to binary, such as from "2 0 2" to "10 000 010"
      
      2. The user enters this memory address by flicking a row of 8 switches to ON,OFF,OFF,OFF,OFF,OFF,ON,OFF to represent the memory address in binary for the previously entered command to reference.
   
   4. The user repeats steps 1 to 4 for ALL the opcodes. For reference, a simple addition program requires 5 opcodes, and a total of  14 entries to load into memory. 

### 3. Execution

After the above steps had been done correctly, the program was only entered into memory. Then the user had to call on the program to use it. In order to do so, the user needs to:

1. Input the numbers to the input addresses, toggling switches for a total of 34 times

2. Toggle the "RESET", then "RUN", then "STOP" switches

3. Set the "DATA/ADDRESSES" switches to go to the output address and "EXAMINE"

4. Results will be displayed on the row of LED lights in binary format, with lights ON for 1 and OFF for 0. 

5. The user copies down the binary output and is required to translate the binary output back to decimal.  

> "If a listener nods his head when you're explaining your program, wake him up. "
> 
> -- FreeBSD Fortune Database

---

## Issues

Clearly, the older computers, with interfaces like the Altair 8800 were designed for advanced users who had a deep grasp on the subject, and its complex usage would likely confuse people without extensive training or experience. Its largest barriers to use in the general public were:

- Requiring the user to memorize a significant portion of a total of 255 different opcodes or constantly refer to a [manual](http://www.emulator101.com/reference/8080-by-opcode.html)

- Slow to use because of the numerous steps necessary to do simple tasks

- Required heavy amounts of math to translate input and output

- Nothing came pre-installed
