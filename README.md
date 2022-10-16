# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: M G gautham 
RegisterNumber:  212221230027
```

## Output:
```
HALF SUBTRACTOR

module HalfSubtractor(A,B,Diff,Borrow);
input A,B;
output Diff,Borrow;
wire x;
xor (Diff, A,B);
not(x,A);
and(Borrow,x,B);
endmodule

FULL SUBTRACTOR

module FullSubtractor(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
wire p;
assign Diff = ((A^B)^C);
not(p,A);
assign Borrow = ((p&B)|(p&C)|(B&C));
endmodule
```
## HALF SUBTRACTOR:

### Logic Symbol:
![image](https://user-images.githubusercontent.com/94810884/196045329-731151ab-bd9d-410a-b9db-95ef2761c798.png)


## Truthtable :
![image](https://user-images.githubusercontent.com/94810884/196045364-31c7f2ab-c3f6-4a8e-8292-888bfb6a76c8.png)


##  RTL realization:
![image](https://user-images.githubusercontent.com/94810884/196045389-4d6d798b-1fd5-4400-9bdc-ecebc64503f7.png)

## Timing diagram :
![image](https://user-images.githubusercontent.com/94810884/196045405-3ff1f4da-22d4-42e8-aaae-687c449cdee9.png)

## Full Subtractor:

## Logic Symbol:
![image](https://user-images.githubusercontent.com/94810884/196045486-c4838149-620b-4e74-848b-12410caa2c91.png)

## Truthtable:
![image](https://user-images.githubusercontent.com/94810884/196045514-90a320e4-f2ca-4cab-a41f-6fc022c049b8.png)

## RTL realization:
![image](https://user-images.githubusercontent.com/94810884/196045559-7bd4bd8a-bd0e-4141-a492-3cb5a6dee066.png)

## Timing diagram:
![image](https://user-images.githubusercontent.com/94810884/196045579-3d732baa-a9b4-4b06-a521-bb4580ee8e83.png)




## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
