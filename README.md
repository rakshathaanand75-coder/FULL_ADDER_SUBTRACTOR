# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: RAKSHATHA S A   
RegisterNumber: 212225220079
*/
```
module exp3_0079(
    input A, B, Cin,
    output SUM, CARRY, BO, DIFF
);

// Full Adder logic
assign SUM = A ^ B ^ Cin;
assign CARRY = (A & B) | (B & Cin) | (A & Cin);

// Full Subtractor logic
assign DIFF = A ^ B ^ Cin;
assign BO = (~A & B) | (B & Cin) | (~A & Cin);

endmodule
```

**RTL Schematic**
<img width="1917" height="1016" alt="image" src="https://github.com/user-attachments/assets/dacc4616-0372-47d5-b5a1-b7ec9bb6c5c8" />


**Output Timing Waveform**
<img width="1600" height="849" alt="WhatsApp Image 2026-09-04 at 7 40 23 PM" src="https://github.com/user-attachments/assets/1677a754-29ad-4cb3-ba21-72b64d690089" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



