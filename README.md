# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
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

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Shankar Saradha  
RegisterNumber: 2122212400252
```
### Half Adder
```python 
module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
```
### Full Adder 
``` python 
module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
## Output 
## Half adder 
<img width="797" alt="ss1" src="https://user-images.githubusercontent.com/93978702/233144739-e46a1c50-200c-469b-83d5-dc86f9bda6fd.png">
<img width="817" alt="ss2" src="https://user-images.githubusercontent.com/93978702/233144818-6a17040d-f3cb-477f-a236-7be45c9f683a.png">
<img width="772" alt="ss3" src="https://user-images.githubusercontent.com/93978702/233144840-a5f17be0-09e5-4e9a-b964-4b3a0a6913c9.png">
## Full adder 
<img width="708" alt="ss4" src="https://user-images.githubusercontent.com/93978702/233144895-7bd89d13-b97a-4d49-9d19-2db9b62a0ac6.png">
<img width="775" alt="ss5" src="https://user-images.githubusercontent.com/93978702/233144932-7696a404-17b1-4195-8839-f0458c210569.png">
<img width="787" alt="ss6" src="https://user-images.githubusercontent.com/93978702/233144954-14006aec-0b91-4b1b-8f99-9e0f338809e3.png">
# Result 
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
