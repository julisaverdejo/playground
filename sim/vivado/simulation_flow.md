# Simulation Flow

Behavioral Simulation
 Is a simulation performed to verify that your design/logic behaves as you expect before synthesis.

To do an RTL simulation you just need the RTL and a testbench.

Post-Synthesis Simulation

> A synthesized netlist is a text-based list of elements of a digital circuit at the gate-level or primitive cells and their connectivity. Essentially, it is a textual description of the digital circuit's schematic

Export a synthesized netlist in Vivado

```
// Synthesis should be performed first
Flow Navigator
	Synthesis -> Run Synthesis -> Open Synthesized Design     -> Schematic
	
File -> Export -> Export Netlist -> Choose EDIF or Verilog format
```

> After schematic is open, netlist can be exported

> I don't know why after perform an RTL simulation, I cannot do a post-synthesis simulation. I have to close vivado and open again

> Do not relaunch post-synthesis simulation, restart and run all.

It looks like you can perform the behavioral simulation, but close it using Tcl Console

```
close_sim -force
```

after that you can run the post-synthesis functional simulation

simulate the synthesized netlist
 synthesized design meets the functional requirements

Post-Implementation Simulation

the synthesized netlist is also used in this simulation

perform functional or timing simulation after implementation.
 design meets functional and timing requirements 