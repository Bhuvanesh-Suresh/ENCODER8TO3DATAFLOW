### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

**Procedure**


1.Type the program in Quartus software.


2.Compile and run the program.


3.Generate the RTL schematic and save the logic diagram.


4.Create nodes for inputs and outputs to generate the timing diagram.


5.For different input combinations generate the timing diagram.


**PROGRAM**
```

Program for Encoder 8 To 3 in Dataflow Modelling and verify its truth table in quartus using Verilog programming. 

Developed by: BHUVANESH S R RegisterNumber:212223240017
//ENCODER 4x2
module ex5(a0,a1,y0,y1,y2,y3);
input y0,y1,y2,y3;
output a0,a1;
assign a1=y3+y2;
assign a0=y3+((~y2)&y1);
endmodule

//DECODER 2x4
module ex5(d0,d1,d2,d3,a,b);
output d0,d1,d2,d3;
input a,b;
assign d0=((~a)&(~b));
assign d1=((~a)&b);
assign d2=(a&(~b));
assign d3=(a&b);
endmodule

//ENCODER 8x3
module ex5(din,a,b,c);
input[0:7] din;
output a,b,c;
assign a=(din[4] | din[5] | din[6] | din[7]);
assign b=(din[2] | din[3] | din[6] | din[7]);
assign c=(din[1] | din[3] | din[5] | din[7]);
endmodule

```


**RTL LOGIC FOR Encoder 4 To 2 in Dataflow Modelling**
![output netlist encoder 4x2](https://github.com/Bhuvanesh-Suresh/ENCODER8TO3DATAFLOW/assets/145742661/a1257128-41d6-4f07-801c-9f5d06c9c458)




**TIMING DIGRAMS FOR Encoder 4 To 2 in Dataflow Modelling**
![output waveform encoder 4x2](https://github.com/Bhuvanesh-Suresh/ENCODER8TO3DATAFLOW/assets/145742661/01ac7a7c-342d-4138-b9a5-5388cd4cd1d5)



**RTL LOGIC FOR Decoder 2 To 4 in Dataflow Modelling**
![output netlist decoder 2x4](https://github.com/Bhuvanesh-Suresh/ENCODER8TO3DATAFLOW/assets/145742661/4d2ab47b-4cfb-42c1-8707-29ca47ffa1af)




**TIMING DIGRAMS FOR Decoder 2 To 4 in Dataflow Modelling**
![output waveform decoder 2x4](https://github.com/Bhuvanesh-Suresh/ENCODER8TO3DATAFLOW/assets/145742661/532213d0-c94d-4018-b0c9-b02e9c4b12fa)




**RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling**
![output netlist](https://github.com/Bhuvanesh-Suresh/ENCODER8TO3DATAFLOW/assets/145742661/8b237412-ce85-4218-ba0d-1a07def58057)



**TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling**
![output waveform](https://github.com/Bhuvanesh-Suresh/ENCODER8TO3DATAFLOW/assets/145742661/e2b3e944-7e8a-40ba-9880-544b29820860)


**RESULTS**

implementing Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables executed succesfully.



