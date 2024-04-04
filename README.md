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
```
module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

and g1(s,ydash,z);
and g2(t,x,y);
and g3(u,w,z);
or g4(f2,s,t,u);
endmodule
```
Developed by:Dhandeeswaran selvakumar
RegisterNumber:212223110009*/


**RTL realization**
![Screenshot 2024-04-04 094721](https://github.com/dhandeeswaran2005/BOOLEAN_FUNCTION_MINIMIZATION/assets/147139188/77fed58a-b428-4092-b128-3f50ca904f67)

**TRUTH TABLE**
![Screenshot 2024-04-04 094730](https://github.com/dhandeeswaran2005/BOOLEAN_FUNCTION_MINIMIZATION/assets/147139188/748a4d7a-5a68-4fd9-993e-bcbd3feae332)

**Timing Diagram**
![Screenshot 2024-04-04 094740](https://github.com/dhandeeswaran2005/BOOLEAN_FUNCTION_MINIMIZATION/assets/147139188/66f64640-a33c-4ebe-a28f-e38b43b8125c)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

