# Verilog AND Gate Design

This project implements an AND Gate using Verilog HDL and was simulated using Vivado.

## Tools Used
- Vivado
- Verilog HDL

## Files
- and_gate.v : Verilog module
- and_gate_tb.v : Testbench
- waveform.png : Simulation result
#### Verilog Code

### and_gate.v
``verilog
module and_gate(
input a,
input b,
output y
);

assign y = a & b;

endmodule
####Testbench
##and_gate_tb;

module and_gate_tb;

reg a,b;
wire y;

and_gate uut(a,b,y);

initial begin
a=0;b=0;
#10 a=0;b=1;
#10 a=1;b=0;
#10 a=1;b=1;
#10 $finish;
end

endmodule

SIMULATION OUTPUT

## Truth Table

A B | Y
0 0 | 0
0 1 | 0
1 0 | 0
1 1 | 1
