# JK_FLIPFLOP
## Aim
To simulate and synthesis JK flipflop using vivado.

## Software Required
Vivado 2023.2 software

## Procedure:
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the run simulation and then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table. 

![image](https://github.com/Douglas0207/JK_FLIPFLOP/assets/166375742/cb5787c3-1c5c-48e5-a831-e382071f9d21)


## Circuit Diagram
![image](https://github.com/Douglas0207/JK_FLIPFLOP/assets/166375742/0cdcb7d7-36c6-4b10-951b-85c791cbc86f)


## Truth Table
![image](https://github.com/Douglas0207/JK_FLIPFLOP/assets/166375742/3116d125-d7a7-45c2-bd1e-357917af4c0c)


## Program
```
module jkff(clk,j,k,rst,q );
input j,k,clk,rst;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
begin
case({j,k})
2'b00: q=q;
2'b01:q=1'b0;
2'b10:q=1'b1;
2'b11:q=~q;
endcase
end
end
endmodule
```
## Output
![image](https://github.com/Douglas0207/JK_FLIPFLOP/assets/166375742/08876632-317d-4f89-9cdd-e3c15c326da7)


## Result
Thus the verilog program for JK flipflop has been simulated and verified successfully.
