# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 

## Logic Diagram
## Procedure
## Program:
## PROGRAM 1:

```
module SUB(a,b,c,d,f);
input a,b,c,d;
output f;
wire f1,f2,f3;
assign f1 = (~c&~b&~a);
assign f2 = (~d&~c&~a);
assign f3 = (c&~(~b)&~a);
assign f= f1&~f2&~f3;
endmodule
```

## RTL VIEW:

![image](https://github.com/RahiniAchudhan/Experiment--02-Implementation-of-combinational-logic-/assets/145742838/3a877492-65b4-4c4a-86f1-405f2b2ea92d)

## TRUTH TABLE:

![image](https://github.com/RahiniAchudhan/Experiment--02-Implementation-of-combinational-logic-/assets/145742838/aa77ae8d-8476-4292-9782-d4324ba58f5c)

## OUTPUT:

![image](https://github.com/RahiniAchudhan/Experiment--02-Implementation-of-combinational-logic-/assets/145742838/97056d09-f9aa-4e4f-8ddc-c02841c4899c)


## PROGRAM 2:
```
module ADD(a,b,c,d,f);
input a,b,c,d;
output f;
wire f1,f2,f3,f4;
assign f1 = c&(~b)&a;
assign f2 = d&(~c)&a;
assign f3 = c&(~b)&a;
assign f4 = ~(f1|f2|f3);
not(f,f4);
endmodule
```
## RTL:
![image](https://github.com/RahiniAchudhan/Experiment--02-Implementation-of-combinational-logic-/assets/145742838/60764413-6200-4393-a59c-79862d088e96)


## TRUTH TABLE:
![image](https://github.com/RahiniAchudhan/Experiment--02-Implementation-of-combinational-logic-/assets/145742838/5b70ae52-3cf6-4d9f-8268-4054c141002d)

## OUTPUT:

![image](https://github.com/RahiniAchudhan/Experiment--02-Implementation-of-combinational-logic-/assets/145742838/24fe3757-52ba-4a65-be51-e5001e2ec383)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
