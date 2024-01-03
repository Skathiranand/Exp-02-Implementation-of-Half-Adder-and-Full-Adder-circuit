### Name:S.Kathir Anand

### Reg No:23013711

# Exp 03 Implementation of Half Adder and Full Adder circuit

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER

### Procedure:

Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

### Program:
```
module Halfadder (a,b,sum,carry);
input a,b;
output sum,carry;
xor (sum,a,b);
and (carry,a,b);
endmodule
```
### Truth Table:
![IMG](https://github.com/Skathiranand/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147141136/45e722d8-4ea2-4a74-a4bc-7b2d3493bf38)

### RTL Realization:
![IMG](https://github.com/Skathiranand/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147141136/c3a7beb7-c571-4fee-a102-4912e1632631)

### Timing Diagram:
![IMG](https://github.com/Skathiranand/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147141136/4056edd7-4f86-46a2-8b2c-6b170c24e6b4)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.
### Program:
```
module Fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b|c& a^ c&b ;
endmodule
```
### Truth Table:
![IMG](https://github.com/Skathiranand/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147141136/56756261-6faa-454e-b4f9-296018c56bab)

### RTL realization:
![IMG](https://github.com/Skathiranand/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147141136/fe41b51f-2244-47d7-866b-6b0676204129)

### Timing Diagram:
![IMG](https://github.com/Skathiranand/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147141136/57575bee-76d3-42a5-b204-380d4a8e20d9)


### Result:
Thus,half adder and full adder are studied and the truth table for different logic gates are verified.
