# Enhanced-Processor
A Lab for ECE243

Part 3:
This part defines a Verilog module named proc, which represents a processor. The processor has inputs for data input (DIN), reset signal (Resetn), clock signal (Clock), run signal (Run), and outputs data output (DOUT), address output (ADDR), and a write signal (W). The processor is controlled by a finite state machine (FSM) described by the Tstep_Q and Tstep_D registers. The FSM controls various operations such as instruction fetching, memory access, ALU operations, and register manipulation.

Part 4:
This part defines a Verilog module named seg7, which presumably represents a 7-segment display controller. It takes inputs for data (Data), address (Addr), select signal (Sel), reset signal (Resetn), and clock signal (Clock). It has outputs representing individual segments of the 7-segment display (H5 through H0). The module contains several instances of the regne module, which appears to be a register with enable control.

Part 5:
This part redefines the proc module with some modifications. Notable changes include the addition of a conditional branch instruction (b), and two new conditional flags (z and c). The conditional flags are used to control branching behavior based on whether the result of the previous ALU operation was zero (z) or if there was a carry out (c). The b instruction enables branching to different locations in the code based on these conditions.

Assembly Code Snippet:
The assembly code snippet provided at the end is an example program written for the processor described in Part 3. It initializes registers r1, r3, and r4 with specific values, enters a loop labeled InLoop, where it stores the value of r1 to the address stored in r3, loads a value from the address stored in r4 to r0, increments r0, increments r1, and then enters another loop labeled IDKLoop. Inside IDKLoop, it sets r2 to 0xff, then enters a delay loop labeled DelayLoop where it decrements r2 until it becomes zero. After the delay loop, it decrements r0 and if it's not zero, it repeats IDKLoop. Finally, it branches back to InLoop and repeats the process.

Explanation:
Overall, the provided code implements a simple processor with a finite state machine controller, along with a 7-segment display controller. The assembly code snippet demonstrates how to write programs for this processor, including simple arithmetic operations, memory access, conditional branching, and looping constructs.
