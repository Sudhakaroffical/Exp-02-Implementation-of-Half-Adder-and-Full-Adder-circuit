# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

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
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: SUDHAKAR K
RegisterNumber:  212222240107
```
### HALF ADDER
```
module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### FULL ADDER
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

### Output:
### RTL

### HALF ADDER

![NO1](https://user-images.githubusercontent.com/118622513/233264505-5311fde1-c967-4610-83dd-88b24b9a093c.png)

### FULL ADDER
![NO2](https://user-images.githubusercontent.com/118622513/233264560-41479cbc-80c2-42e5-9e94-67d7b4009927.png)


### TIMING DIAGRAM
### HALF ADDER
![NO3](https://user-images.githubusercontent.com/118622513/233264661-2614d8aa-2591-44c6-acd4-a3ac8b7df523.png)

### FULL ADDER

![NO4](https://user-images.githubusercontent.com/118622513/233266514-96e58bb5-7909-478f-b919-927dd88fac0e.png)


### TRUTH TABLE 
### HALF ADDER
![NO5](https://user-images.githubusercontent.com/118622513/233264782-11fe8787-b613-433f-8380-519080f16174.png)

### FULL ADDER

![WhatsApp Image 2023-04-20 at 10 54 30](https://user-images.githubusercontent.com/118622513/233266114-92620015-471a-45ba-b24f-f26aae3d6945.jpg)





### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
