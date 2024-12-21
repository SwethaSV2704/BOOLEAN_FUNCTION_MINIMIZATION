# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: SWETHA S V RegisterNumber: 24000297 */

```
module de2(a,b,c,d,w,x,y,z,f1,f2);

input a,b,c,d,w,x,y,z;

output f1,f2;

wire m,n,o,p,q,r,s,t,u,k1,k2,k3,k4,k5,k6,k7,k8,k9;

not(m,a);

not(n,b);

not(o,c);

not(p,d);

and(q,m,n,o,p);

and(r,a,o,p);

and(s,n,c,p);

and(t,m,b,c,d);

and(u,b,o,d);

or(f1,q,r,s,t,u);

not(k1,w);

not(k2,x);

not(k3,y);

not(k4,z);

and(k5,x,k3,z);

and(k6,k2,k3,z);

and(k7,k1,x,y);

and(k8,w,k2,y);

and(k9,w,x,y);

or(f2,k5,k6,k7,k8,k9);

endmodule

```
**RTL realization**
![Screenshot 2024-12-21 133520](https://github.com/user-attachments/assets/51a27ae6-e5a9-4c3c-8596-87485a5caab0)

**Logic symbol & Truth Table**
![Screenshot 2024-12-21 133606](https://github.com/user-attachments/assets/f6e945e5-ba9a-490a-9aa3-c8edb66e3558)


**Timing Diagram**
![Screenshot 2024-12-21 135912](https://github.com/user-attachments/assets/edc52ebb-f406-42d6-9a70-7b63bf0151a0)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

