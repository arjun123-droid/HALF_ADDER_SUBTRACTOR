# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
![WhatsApp Image 2025-11-18 at 11 46 44_9975983f](https://github.com/user-attachments/assets/85cdc7ee-1025-4f2a-9781-7a105850ac3e)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
```
Developed by:Arjun.R.S
RegisterNumber: 25017547
```

**Half Adder:**
```
module half_adder(sum, carry, a, b);
  output sum;
  output carry;
  input a;
  input b;
  assign sum = a ^ b;
  assign carry = a & b;
endmodule
```
**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot 2025-11-18 112440" src="https://github.com/user-attachments/assets/f536f7f8-067b-402d-bbe9-c7eb2049460a" />

**Output/TIMING Waveform**

<img width="1920" height="1080" alt="Screenshot 2025-11-18 112828" src="https://github.com/user-attachments/assets/f3784a1e-a977-4848-925e-8bef75ddd057" />

**Half subtractor:**
```
module half_subtractor(diff, borrow, a, b);
  output diff;
  output borrow;
  input a;
  input b;
  assign diff = a ^ b;
  assign borrow = ~a & b;
endmodule
```
**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot 2025-11-18 113814" src="https://github.com/user-attachments/assets/2ec8b476-dcf1-4115-b1ad-d1c4a592f13b" />

**Output/TIMING Waveform**
<img width="1920" height="1080" alt="Screenshot 2025-11-18 114514" src="https://github.com/user-attachments/assets/f518c2eb-31e1-4394-83c7-a6ae8883c603" />

**Result:**
Thus To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming is successfully executed.
