```
Name : R.Jayamani
Reg no: 212222100014
```
# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

 
 
 
## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Hardware:

PCs, Cyclone II , USB flasher

## Software

Quartus prime


### Theory

### Introduction

Logic gates are the basic building blocks of any digital system. Logic gates are electronic circuits having one or more than one input and only one output. The relationship 
between the input and the output is based on a certain logic. Based on this, logic gates are named as - AND gate,OR gate,NOT gate,NAND gate,NOR gate,Ex-OR gate,Ex-NOR gate.

### 1) AND gate

The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB

Y= A.B

### 2) OR gate

The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation.

Y= A+B

### 3) NOT gate

The NOT gate is an electronic circuit that produces an inverted version of the input at its output. It is also known as an inverter. If the input variable is A, the inverted output is known as NOT A. This is also shown as A' or A with a bar over the top, as shown at the outputs.

Y= A'

### 4) NAND gate

This is a NOT-AND gate which is equal to an AND gate followed by a NOT gate. The outputs of all NAND gates are high if any of the inputs are low. The symbol is an AND gate with a small circle on the output. The small circle represents inversion.

Y= (AB)’

### 5) NOR gate

This is a NOT-OR gate which is equal to an OR gate followed by a NOT gate. The outputs of all NOR gates are low if any of the inputs are high. The symbol is an OR gate with a small circle on the output. The small circle represents inversion.

Y= (A+B)’

### 6) Ex-OR gate

The 'Exclusive-OR' gate is a circuit which will give a high output if either, but not both of its two inputs are high. An encircled plus sign (⊕) is used to show the Ex-OR operation.

Y= A⊕B

### 7) Ex-NOR gate

The 'Exclusive-NOR' gate circuit does the opposite to the EX-OR gate. It will give a low output if either, but not both of its two inputs are high. The symbol is an EX-OR gate with a small circle on the output. The small circle represents inversion.

Y= A⊕B

## Procedure

Connect the supply (+5V) to the circuit

Switch ON the main switch

Press the switches for inputs “A” and “B”. The switch is ON state when 1 is pressed. The switch is OFF state when 0 is pressed.

If the output is 1, then the bulb glows.

Check all the gates following the same procedure.

## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Jayamani.R
Register Number: 212222100014
*/
```
module Experiment2(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=A&(~C)&(~D);
assign x3=(~B)&C&(~D);
assign x4=(~A)&B&C&D;
assign x5=B&(~C)&D;
assign F1=x1|x2|x3|x4|x5;
endmodule

```

## Truth Table:
![Screenshot 2023-08-26 090427](https://github.com/Jayamani25/Experiment--02-Implementation-of-combinational-logic-/assets/85949888/a5457716-8e63-468f-98ce-603969310dbc)


## RTL realization:
![Screenshot 2023-08-26 090508](https://github.com/Jayamani25/Experiment--02-Implementation-of-combinational-logic-/assets/85949888/fa607b5b-60b3-465b-adcf-266a55c52796)

## Output:
![Screenshot 2023-08-26 093431](https://github.com/Jayamani25/Experiment--02-Implementation-of-combinational-logic-/assets/85949888/b2b34d86-bc07-462f-bbe4-0db178bbcea0)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
