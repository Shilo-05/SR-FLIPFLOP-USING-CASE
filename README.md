# SR-FLIPFLOP-USING-CASE

```
Name: Oswald Shilo
Reg: 212223040139
```

## **AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

## **SOFTWARE REQUIRED:**

Quartus prime

## **THEORY**

* SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

 
* This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.


 
* Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

 
* By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.


* The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

## **Procedure**

* Open Quartus Prime: Create a new project in Quartus Prime and set up your working directory, specifying the device family and specific FPGA model if needed.

* Write the Verilog Code: Open a new Verilog file and input the SR flip-flop code. Define inputs s, r, clk, and outputs q, qbar as given in the program. Use the always block to specify the behavior on the positive clock edge.

* Compile the Code: Save the Verilog file, then compile it within Quartus Prime to check for syntax errors and ensure successful compilation.

* Simulate the Design: Go to the simulation settings in Quartus, configure the inputs (s, r, and clk), and run the simulation to observe the changes in output (q, qbar) with respect to the inputs and clock transitions.

* Verify the Output: Compare the simulation results with the truth table for the SR flip-flop to validate correct functionality.


## **PROGRAM**

**/* Program for flipflops and verify its truth table in quartus using Verilog programming.*/
**
```
module Exp_06(s,r,clk,q,qbar);
input s,r,clk;
output reg q;
output reg qbar;
initial 
begin
q=0;
qbar=1;
end
always @(posedge clk)
begin
   q=s|(~r&q);
   qbar=r|(~s&~q);
end
endmodule

```

## **RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/user-attachments/assets/3358dc97-84f6-477f-a31a-ec8ed09dc2de)


## **TIMING DIGRAMS FOR FLIP FLOPS**

![image](https://github.com/user-attachments/assets/ffb43aa4-5ae6-4c45-9d7d-fb00a0436f6c)



## **RESULTS**

The Output for **SR-FLIPFLOP-USING-CASE** is Verified Successfully.

