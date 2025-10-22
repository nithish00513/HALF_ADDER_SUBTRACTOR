# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

![DE TT 1](https://github.com/user-attachments/assets/974d874d-88fe-44ae-98a4-2b5652837a76)

![DE TT 2](https://github.com/user-attachments/assets/55e1b114-e022-484e-b027-bab33e040c06)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Nithish Kumar S 

RegisterNumber: 212224230190
*/

```
module ex03(a,b,cy, sm, df,bo);
input a,b; 
output sm,cy, df, bo;
xor(sm,a,b);
and(cy,a,b); xor(df,a,b);
and (bo,~a,b);
endmodule
```

**RTL Schematic**

![DE RTL 3](https://github.com/user-attachments/assets/44e63efd-9a71-46c1-bf7a-745d3b50465a)


**Output/TIMING Waveform**

![DE WAVEFORM3](https://github.com/user-attachments/assets/02780363-d136-4230-97d5-7337671ba607)


**Result:**

Thus designing a half adder and half subtractor circuit and its truth table is verified in Quartus using Verilog programming.
