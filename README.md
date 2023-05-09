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
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming

Developed by: LOKESH KUMAR P
RegisterNumber: 212222240054

### HALF ADDER:
```
module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

```

### FULL ADDER:

```
module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule

```

### Output:

### Half Adder:
### RTL


![Screenshot 2023-05-09 134940](https://user-images.githubusercontent.com/119644432/237039442-bcc79e57-58b5-4bb4-bd52-c944995d75a8.png)

### TIMING DIAGRAM


![Screenshot 2023-05-09 134958](https://user-images.githubusercontent.com/119644432/237039616-a2fb1256-926c-4ca3-bd01-769304a6a663.png)


### TRUTH TABLE 


![Screenshot 2023-05-09 135012](https://user-images.githubusercontent.com/119644432/237039783-f9faac9c-1382-4c88-b896-ea6f04ed6d51.png)





### Full Adder:

### RTL

![Screenshot 2023-05-09 140053](https://user-images.githubusercontent.com/119644432/237040347-571d873a-11be-4fc4-87d2-cef84c52edf4.png)

### TIMING DIAGRAM

![Screenshot 2023-05-09 140227](https://user-images.githubusercontent.com/119644432/237040977-0ced205d-09c9-4ae4-b02c-ac707e57a1c0.png)



### TRUTH TABLE 

![Screenshot 2023-05-09 140241](https://user-images.githubusercontent.com/119644432/237041078-62a017a3-1943-465c-8f90-b8d0f94058e3.png)



### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
