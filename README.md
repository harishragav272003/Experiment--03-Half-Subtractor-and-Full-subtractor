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


## Programs:
module halfsub(A,B,diff,borrow);
input A,B;
output diff,borrow;
assign diff=(A^B);
assign borrow=(~A&B);
endmodule

module fullsub(X,Y,Z,Borrow,Difference); 
input X,Y,Z;
output Borrow,Difference;
assign Difference = (X^Y^Z);
assign Borrow = (~X&(Y^Z)|(Y&Z)); 
endmodule

/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: HARISH RAGAV S
RegisterNumber:  22008415
*/

## Output:

## Truthtable
![image](https://user-images.githubusercontent.com/119345345/211159775-6889757d-5668-48ae-85e0-20bfa4b59eb9.png)

![image](https://user-images.githubusercontent.com/119345345/211159783-bc07046d-0b85-4922-b6c3-bbb166af20b3.png)



##  RTL realization
![image](https://user-images.githubusercontent.com/119345345/211159818-6064c8b8-152b-499a-a555-13d25bb591d5.png)

![image](https://user-images.githubusercontent.com/119345345/211159837-d0f41cbc-7f26-43e8-994d-fcddb5d0b747.png)



## Timing diagram 

![image](https://user-images.githubusercontent.com/119345345/211159877-8b731187-18e7-4e56-b27e-e5c9caacc537.png)

![image](https://user-images.githubusercontent.com/119345345/211159922-969b0632-cd83-4619-959d-793f21ad16fa.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
