### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**PROGRAM**
```
module syn13(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
    if(!rstn)
	    out<=0;
	 else
	    out <= out+1;
end
endmodule

```

Developed by:T K SHRIVIMAL

RegisterNumber:24003314

**RTL LOGIC UP COUNTER**

![396369690-a636d1c0-9304-40c7-b7e7-5982b3f850de](https://github.com/user-attachments/assets/bcde794b-fab6-4f1a-96d0-cb56d3d0b916)

**TIMING DIAGRAM FOR IP COUNTER**

![396369762-adb470cb-6ed2-489f-8d17-78f4e5b12180](https://github.com/user-attachments/assets/2c8484d0-0817-4c1f-a188-3056e0461e80)

**TRUTH TABLE**

![396552980-a277d660-9342-408c-9590-5bbf5f0accb6](https://github.com/user-attachments/assets/9310323f-3af1-45ad-9970-0f71fcc32c94)

**RESULTS**

Thus 4 bit synchronous up counter and validate functionality are verified Successfully.
