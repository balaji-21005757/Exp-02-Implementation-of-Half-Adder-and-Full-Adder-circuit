# Exp:03 Implementation of Half Adder and Full Adder circuit

# Implementation of Half Adder and Full Adder circuit
## Aim:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime
## Theory:
Adders are digital circuits that carry out addition of numbers.

## Half Adder:
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.
```
Sum = A’B+AB’ =A ⊕ B Carry = AB
```
## Full Adder:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.
```
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
```
 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

### Figure:01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Figure:02 FULL ADDER 

## Procedure:

1. Connect the supply (+5V) to the circuit.
2. Switch ON the main switch.
3. If the output is 1, then the led glows.
## Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Balaji K
RegisterNumber:  212221230011
```
## Half Adder:
```
module Experiment03(A,B,S,C);
input A,B;
output S,C;
assign S=A^B;
assign C=A&B;
endmodule
```
## Full Adder:
```
module EX03(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
### Logic symbol:
#### Half Adder:
![image](https://github.com/SOMEASVAR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93434149/5a70bf04-3daa-4ac8-baa4-fe17f8798f93)
#### Full Adder:
![image](https://github.com/SOMEASVAR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93434149/a94d607b-ca92-483f-ba7d-b5e29825d99d)
### Truth Table:
#### Half Adder:
![image](https://github.com/SOMEASVAR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93434149/92d78afd-f4ea-4749-89bb-5f3772cd36ea)

#### Full Adder:
![image](https://github.com/SOMEASVAR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93434149/89f3b412-4151-4ef1-987d-fbfef10ef14f)
## Output:
## RTL DIAGRAM:
### Half Adder:
![image](https://github.com/SOMEASVAR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93434149/af4a3459-2e34-4e09-9158-0beb4a8d062d)

### Full Adder:
![image](https://github.com/SOMEASVAR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93434149/38dc3ee1-ddbd-4f33-9d21-e66013267f5e)



## TIMING DIAGRAM:
### Half Adder:
![image](https://github.com/SOMEASVAR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93434149/2c55d3e3-9c73-4fcf-a4b4-36402051c726)

### Full Adder:
![image](https://github.com/SOMEASVAR/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93434149/8d1ebf2c-0a93-40e0-9455-e6a61f1c6e7e)
## Result:
Thus the given logic functions are implemented using half adder and full adder with their operations are verified using Verilog programming.
