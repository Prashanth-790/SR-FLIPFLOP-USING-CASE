# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**:

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**:
 1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. Generate the timing diagram for different input combinations.



**PROGRAM**:

 developed by :  lakshmen prashanth R
 
 reg no :  24007066

```
module exp(s, r, clk, q, qbar);
  input s, r, clk;
  output reg q, qbar;
  initial begin
    q = 0;
    qbar = 1;
  end
  always @(posedge clk) begin
    if (s & r) begin
      q = 1'bx;
      qbar = 1'bx;
    end else if (s) begin
      q = 1;
      qbar = 0;
    end else if (r) begin
      q = 0;
      qbar = 1;
    end
  end
endmodule
```

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL LOGIC FOR FLIPFLOPS**:
![Screenshot 2025-01-01 203935](https://github.com/user-attachments/assets/dc7d1c0a-51e7-49e1-b99a-e1ecdf27db96)


**TIMING DIGRAMS FOR FLIP FLOPS**:

![Screenshot 2025-01-01 204114](https://github.com/user-attachments/assets/8c6a44b0-7be4-420e-9efc-e9443c9e75c7)


**RESULTS**:

Thus, the SR flip-flop was implemented using Verilog, and its functionality was validated using functional tables.
