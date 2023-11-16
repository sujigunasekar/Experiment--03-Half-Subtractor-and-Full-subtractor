# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime
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
STEP 1: Use module project name(input,output) to start the Verilog programmming.

STEP 2: Assign inputs and outputs using the word input and output respectively.

STEP 3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

STEP 4: Use each output to represnt onre for differnce and the other for borrow.

STEP 5: End the verilog program using keyword endmodule.


# Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Suji.G
RegisterNumber:  212222230152

### PROGRAM FOR HALF SUBTRACTOR:
module exp4(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule

### PROGRAM FOR FULL SUBTRACTOR:
module exp40(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign difference=(a^b^c);
assign borrow=(~a&(b^c)|(b&c));
endmodule
```

# Output:
# Truthtable
### HALF SUBTRACTOR
![Screenshot 2023-09-08 091542](https://github.com/sujigunasekar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559822/84f21469-9d39-49bb-bcdf-ae1ff237d1ba)
### FULL SUBTRACTOR
![Screenshot 2023-09-08 091551](https://github.com/sujigunasekar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559822/0d9e16e8-693c-4334-b7eb-e97d88bf850a)
##  RTL realization
### HALF SUBTRACTOR
![Screenshot 2023-09-08 084257](https://github.com/sujigunasekar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559822/fdfa6e9c-8c3c-4193-a1a4-8560729ec2f0)
### FULL SUBTRACTOR
![Screenshot 2023-09-08 085445](https://github.com/sujigunasekar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559822/3c50ed57-27d6-4f28-98a3-9c8f87f5ff7e)
## Timing diagram 
### HALF SUBTRACTOR
![image](https://github.com/sujigunasekar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559822/a66d0b26-e615-49c1-ba3c-526b24a032d4)
### FULL SUBTRACTOR
![Screenshot 2023-09-08 090343](https://github.com/sujigunasekar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559822/f5bf64dc-63db-476e-bc5e-c009b58aeb2d)

# Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
