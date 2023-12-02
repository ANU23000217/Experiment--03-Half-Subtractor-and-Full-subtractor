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

## Procedure :
STEP 1:
Use module program name (input , output ) to start the verilog programming. 

STEP 2 :
Assign inputs and outputs.

STEP 3:
End the verilog program using keyword endmodule.



## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: ANU RADHA .N

RegisterNumber:  23000217
*/

Half Subtractor :
```
module halfsub(output b ,d,input x,y);
assign d = x^y;
assign b = ~x&y;
endmodule 
```
 Full Subtractor :
 ```
module fullsub (output b , d, input x , y,z);
assign d = x^y^z;
assign b = ~x&(y^z)|y&z;
endmodule 


```

 ## Output:

## Truthtable :

Half Subtractor:

![Screenshot 2023-12-02 134912](https://github.com/ANU23000217/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/139117108/80075f42-81bd-4441-a3ee-801edcc6225e)

 Full Subtractor:
 
![Screenshot 2023-12-02 135032](https://github.com/ANU23000217/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/139117108/e9da1ff5-ae0b-4294-b70a-209a9ef644e6)

##  RTL realization

Half Subtractor:
![WhatsApp Image 2023-12-02 at 10 30 52_269938d2](https://github.com/ANU23000217/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/139117108/6644175e-ba8a-45b3-a9cf-9817a0a8472a)


 Full Subtractor:
 
 ![WhatsApp Image 2023-12-02 at 10 34 59_236351bf](https://github.com/ANU23000217/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/139117108/7168dcda-6237-4aea-ba7c-59421f02edda)


## Timing diagram 

Half Subtractor :
![Screenshot 2023-12-02 135923](https://github.com/ANU23000217/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/139117108/4775455b-f738-49f3-b41f-87223f972059)



 Full Subtractor:
 ![Screenshot 2023-12-02 140604](https://github.com/ANU23000217/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/139117108/034f530e-6984-4ec7-9f27-7883c70a481b)

 
## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
