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

**Full Adder**

![image](https://github.com/pochireddyp/FULL_ADDER_SUBTRACTOR/assets/150232043/890b8394-6041-4283-ae00-c2882c1d2412)

**Full Subtractor**

![image](https://github.com/pochireddyp/FULL_ADDER_SUBTRACTOR/assets/150232043/4133b876-b000-45ed-8bfb-2fc6c63b69a7)




**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

**Developed by:pochireddy.p**

**RegisterNumber:212223240115**

*/
```
module full_addersub(a,b,c,sum,carry,D,Bo);
input a,b,c;
output sum,carry,D,Bo;
assign sum = a^b^c;
assign carry = (a&b)|(b&c)|(a&c);
assign D = a^b^c;
assign Bo = (~a&b)|(b&c)|(~a&c);
endmodule

```

**RTL Schematic**

![image](https://github.com/pochireddyp/FULL_ADDER_SUBTRACTOR/assets/150232043/8cf59265-1945-4457-87af-80623bed889c)

**Output Timing Waveform**

![image](https://github.com/pochireddyp/FULL_ADDER_SUBTRACTOR/assets/150232043/f1349cef-cf43-4438-86b4-2f95c046ce80)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



