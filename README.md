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

**Procedure**1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.



**Program:**module fulladd1(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor g1(sum,a,b,c);
assign carry=(a&b)|(b&c)|(c&a);
endmodule 


module fullsub01(a,b,c,diff,borrow);
input a,b,c;
output diff,borrow;
xor g1(diff,a,b,c);
assign borrow=((~a&c)|(~a&b)|(b&c));
endmodule 
Developed by:Lavanya.A register no:25007878


**RTL Schematic**
<img width="1919" height="1074" alt="Screenshot 2025-11-17 132748" src="https://github.com/user-attachments/assets/2cddcc84-2aeb-409e-b69b-b081e6c8400b" />
<img width="1912" height="1068" alt="Screenshot 2025-11-17 133930" src="https://github.com/user-attachments/assets/d0d47a2c-7751-42cf-b726-7f6ee4806da8" />




**Output Timing Waveform**
<img width="1915" height="1074" alt="Screenshot 2025-11-17 132959" src="https://github.com/user-attachments/assets/a3df52bb-b5f3-4727-b301-d8d62cd62c5f" />
<img width="1913" height="1068" alt="Screenshot 2025-11-17 134304" src="https://github.com/user-attachments/assets/4ba946c5-0d6e-4b2e-b1de-53a6661d9ce3" />




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



