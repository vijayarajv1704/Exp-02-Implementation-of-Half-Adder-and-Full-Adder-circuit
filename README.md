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

/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: VIJAYARAJ V
RegisterNumber:212222230174
*/

## HALF ADDER

module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

## FULL ADDER

module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule

### Output:

### RTL

###HALF ADDER

![image](https://user-images.githubusercontent.com/121303741/234765651-32e1006d-1789-4859-8c40-b215b5e7d07e.png)

###FULL ADDER

![image](https://user-images.githubusercontent.com/121303741/234765738-a92420c2-cfcd-4e3b-b716-179b594f20bc.png)

### TIMING DIAGRAM

# HALF ADDER

![image](https://user-images.githubusercontent.com/121303741/234765823-577df5e6-bbe9-4aa6-900f-47f47095b9d9.png)

# FULL ADDER 

![image](https://user-images.githubusercontent.com/121303741/234765925-54b9c86b-e881-47e8-8e24-ce3e8b3cb250.png)

### TRUTH TABLE 

### HALF ADDER

![image](https://user-images.githubusercontent.com/121303741/234765990-50bce168-7ee3-45c8-8726-c01bd147b5be.png)

### FULL ADDER

![image](https://user-images.githubusercontent.com/121303741/234766086-74e740d5-a7eb-4312-a35a-463fff6140c2.png)

### Result:

Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.


