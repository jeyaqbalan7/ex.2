### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
![image](https://github.com/jeyaqbalan7/ex.2/assets/119393851/cd7399cb-940f-4b5f-9013-3e1e78b793f1)

![image](https://github.com/jeyaqbalan7/ex.2/assets/119393851/7e338dac-f2e4-40f0-9b12-b7b2201f23cd)

## Truth Table:
![image](https://github.com/jeyaqbalan7/ex.2/assets/119393851/b7a082be-b9e3-41d6-93bf-b91ffa3aa96c)

![image](https://github.com/jeyaqbalan7/ex.2/assets/119393851/90f647a9-890b-4def-90b7-8a39b5a31cc6)


## Program:
```
module exp2a(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire adash,bdash,cdash,ddash,x,y,z,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(x,bdash,ddash);
and(y,adash,b,d);
and(z,a,b,cdash);
or(f1,x,y,z);
and(p,cdash,d);
and(q,a,c);
and(r,b,c);
or(f2,p,q,r);
endmodule
```

## RTL Schematic:
![image](https://github.com/jeyaqbalan7/ex.2/assets/119393851/105b6ffd-5037-4b2a-b2e6-00c9759fa145)

## Timing Diagram:
![image](https://github.com/jeyaqbalan7/ex.2/assets/119393851/453c1514-1358-4f9e-a7c9-62a95bae4fea)

## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



