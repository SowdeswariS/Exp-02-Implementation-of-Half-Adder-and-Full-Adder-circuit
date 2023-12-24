## Name: Sowdeswari S
## Register number: 212223050051

# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit

### AIM:


To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.


### Equipments Required:


Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime


## Theory

Adders are digital circuits that carry out addition of numbers.

### Half Adder


Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB


#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)


### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.


### Program:


module HA(a,b,Sum,Carry);

input a,b;

output Sum,Carry;

xor(Sum,a,b);

and(Carry,a,b);

endmodule


## Truthtable



![Screenshot 2023-12-24 125445](https://github.com/SowdeswariS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154341385/e6597bc1-deeb-42bc-92e8-a6fe664cf809)



## RTL 


![Screenshot 2023-12-24 121921](https://github.com/SowdeswariS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154341385/624a7746-ab2c-4bf1-84de-8bd790d33af7)



### TIMING DIAGRAM:



![Screenshot 2023-12-24 122343](https://github.com/SowdeswariS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154341385/26a9d774-9de5-4d71-ac3a-b9213d93b47b)





### Full Adder:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin


#### Figure -02 FULL ADDER 


 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)


 
### Procedure


Connect the supply (+5V) to the circuit

Switch ON the main switch

If the output is 1, then the led glows.


### Program:

module FA(a,b,c,sum,carry);

input a,b,c;

output sum,carry;


xor(sum,a,b,c);

assign carry=a&b|b&c|c&a;

endmodule


## Truth table



![Screenshot 2023-12-24 125950](https://github.com/SowdeswariS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154341385/46239ea1-3a92-41b6-9db4-32caa1babe1c)




## RTL realization



![Screenshot 2023-12-24 125332](https://github.com/SowdeswariS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154341385/ba7f0744-6dd5-4a7a-b46f-824d3d36b10b)



### TIMING DIAGRAM



![Screenshot 2023-12-24 130812](https://github.com/SowdeswariS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154341385/7a2d06f3-227f-4908-9a24-4dfec1f247a7)




### Result:


Thus the given half adder and full adder circuit is implemented and verified using Verilog programming.

