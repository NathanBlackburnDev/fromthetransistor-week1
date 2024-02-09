# Theory of transistors, about FPGAs and ICs
This README talks is from week 1 of [from the transistor by geohot](https://github.com/geohot/fromthetransistor). It talks about transistors, FPGAs, ICs and the electrical components/concepts needed to understand the content.
## What are transistors?
Transistors are small electronic components with two main functions: switch circuits on or off and amplify signals. Small lower power transistors will be in a resin case but a higher power transistor will have a metal/resin case which is used to remove the heat from the transistor. Transistors have 3 pins, 1 is the emitter (E), 1 is the base (B) and the final one is the collector (C). The emitter serves as the source of electrons, the base as the control terminal (essentially it controls the flow of electrons through the transistor) and collector which is the drain for the electrons. 
### Why use transistors?
If you make a electrical circuit which consists of only a battery and a light (and of course, a wire to connect the two) the light will be constantly on, you can turn the light off by making a switch but this requires the human to manually control the switch, so to automate this process you can use a transistor. When you add the transistor, the transistor will be blocking the flow of current, however if you provide a small voltage to the base then the transistor will start to allow current to flow in the main circuit meaning that the light will turn on. Typically you need to apply 0.6 - 0.7v to the base pin to turn the transistor on. If you provide lower voltage like 0.6v then the transistor could turn on but it is not allowing much current to flow through the main circuit, but if you apply more voltage like 0.8v then the transistor will be allowing all current to flow through the main circuit meaning the transistor is fully open. This way you are using a small voltage and current (the voltage being provided to the base of the transistor) to control a larger voltage and current (the main circuit). Because of this, if you provide a large input signal in the main circuit and then provide a smaller input signal to the base of the transistor then the transistor works as an amplifier. 

Typically there is a very small current on the base of the transistor and the collector has a much larger current, the ratio between these two can be defined as the following:
β = Collector current / Base current

For example if the base current (the current going into the base of the transistor) was 1mA and the collector current was 100mA then β would be 100. You can rearrange this formula to find the currents:
Collector current = β * Base current
Base current = collector current / β
### How do transistors work?
There are two main types of bipolar-junction transistors (BJT), the PNP and the NPN. 

![NPN](https://github.com/NathanBlackburnDev/transistors/assets/116575260/e9b95c05-a7db-4883-b496-87589eb15a8f)

With the NPN you have both the main circuit and the control circuit, both are connected to the positive side of the battery. The main circuit is off until we turn the switch on, current will flow through both wires to the transistor, however if you remove the main circuit (highlighted in green) the control circuit LED will still turn on when the switch is pressed as the current is returning to the battery through the transistor. The control circuit has 5mA flowing into the base pin, the main circuit has 20mA flowing into the collector and the current coming out of the emitter is 25mA, meaning that all the mA in this entire circuit all add together.

![PNP](https://github.com/NathanBlackburnDev/transistors/assets/116575260/48db5c7e-bd22-4aee-a0d9-05745c10ff8c)

In this PNP circuit, the emitter is connected to positive of the battery rather than the emitter being connected to the negative of the battery like the NPN circuit. The main circuit is off until you press on with the switch, with this circuit some of the current flows out of the base and into the battery (the black wire). If you remove the main circuit (again, highlighted in green) the main circuit will still turn on. When the switch is on, there are 25mA flowing into the emitter, the main circuit has 20mA flowing through, out of the collector and the control circuit has 5mA flowing through out of the base. The current therefore divides in the PNP transistor, as opposed to the NPN transistor where the current is all combined.

Diagrams use conventional current whereby the current flows out of the positive side of the battery and then out of the emitter into the negative side of the battery, but electron flow, where its actually the opposite and the current flows out of the negative side into the emitter and then out of the current and the base into the positive side of the battery.



![NPN w current](https://github.com/NathanBlackburnDev/transistors/assets/116575260/277ef9ad-d7ce-41cd-8bcc-cb37ceb13adc) ![PNP w current](https://github.com/NathanBlackburnDev/transistors/assets/116575260/80db2f88-9588-4a3e-9a20-426a2c0009db)

On the top in the NPN, you can see the current (green arrows) flowing out of the negative side of the battery and inside the positive, but on the bottom in the PNP the opposite is happening where the current goes into the negative side and out the positive.

### Transistor materials
Transistors are made out of semi conductor materials such as sillicon and germanium, however both materials have almost no free moving electrons so they are doped with impuraties and other materials which changes its electrical property. This is called _P-type_ and _N-type_ doping. We combine the now doped sillicon materials to form the P-N junction. We can combine the P-type and N-type sillicon to make the NPN or PNP transistors. When the doped sillicon have been merged to make the P-N junction, one side the pieces will have no electrons (P side) and the other (N side), will have too many electrons causing a _depletion region_. In the depletion region some of the excess electrons from the N-side will move over to the holes on the P-side and vice versa. This migration will cause a build up with electrons and holes on opposite sides. The electrons that move over to the P-side become slightly negatively charged and the holes that move over to the N-side become slightly positively charged. This build up then creates a slightly negatively and slightly positively charged region which creates an electic field, preventing any electrons from coming through. The difference in this electric field is typically 0.7v.

### Forward bias
When you connect a voltage source across the two ends, with the positive source hooked up to the P-type side and the negative to the N-type side, this will create a forward bias and electrons will flow through the N-type to the P-type and back into the positive voltage source. The voltage source must be 0.7v or greater in order for the electrons to flow through.

### Reverse bias
When you swap the voltage source around so the N-type is hooked to the positive source and the negative to the P-type, the electrons in the electric field will be pulled back to their respective sides, where the holes are held back to the P-type and the electrons back to the N-type which causes the reverse bias.

## Integrated circuits
IC is a collection of electronic components such as 
### Resistors
The resistor is a passive electrical component that creates resistance in the flow of electric current. They are used in almost all electrical networks and electronic circuits. The resistance is measured in ohms (Ω). Electrical flow will pass through the resistor and the resistor will restrict the flow of the electric current. You can think of it like water flowing through a wide pipe, if the pipe at some point becomes very short the the resistance of the flowing water increases and thus less water comes through, the same applies here.

![Screen Shot 2024-02-09 at 16 57 30 pm](https://github.com/NathanBlackburnDev/transistors-FPGAs-ICs/assets/116575260/120cc707-0f08-418e-95d2-1f3356bbbc19)

The voltages between two points is equal to the current between the two points * the voltage
### Capacitors
A capacitor is similar to a battery, with the main difference being 
### Logic gates
Computers user logic gates to transform the 1s and 0s from input wires. A logic gate accepts input then outputs a result based on their state.
Some logic gates:
- NOT: is an inveter. If input is 1 then output is 0 and vice versa

![Screen Shot 2024-02-09 at 18 35 43 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/ca7825fe-8e92-4480-8cc2-79512cdd6424)

- OR: as long as either input is 1 then output will be 1

![Screen Shot 2024-02-09 at 18 36 13 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/755ec884-c94e-4391-9c12-ead3bd6ce196)

- AND: both inputs need to be 1 for output to be 1, if both input is 0 or one input is 1 and the other 0 then output will be 0

![Screen Shot 2024-02-09 at 18 36 36 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/d81e2e8a-e256-481b-866a-dda33b9f2f6e)

- NAND (NOT AND): output 0 if all inputs are 1
  
![Screen Shot 2024-02-09 at 18 37 14 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/6ca80383-9299-4090-8670-5d949af34f33)

- XOR: output 1 only when one input out of its inputs is 1. If both inputs are 0 then output is 0, if both outputs are 1 then output is 0, if output is 1 0 then output is 1
  
![Screen Shot 2024-02-09 at 18 37 36 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/8abe82b7-bcb8-4d82-8dc2-5c99532742ac)

- NOR: output 1 is both inputs are 0. if one input is 1 and one is 0, output is 0. Is the inverse of AND

![Screen Shot 2024-02-09 at 18 37 56 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/f7f284c0-cc89-420c-8487-3b532864cab7)
  
### Flip-flops
Flip-flop is a circuit that maintains a state until directed by input to change the state. A basic flip-flop can be constructed using four-NAND or four-NOR gates. Flip flop is popuarly known as the basic digital memory circuit. It has 2 states, 1 and 0. A flip-flop is a sequential circuit that consists of single binary state of information/data. 
## What are FPGAs?
Field Programmable Gate Arrays (FPGAs) are semiconductor devices that are based around a matrix of configurable logic blocks (CLBs) connected via programmable interconnects that allow the designer to connect blocks and configure them to perform everything from simple logic gates to complex functions. FPGAs can be reprogrammed to desired application or functionality requirements after manufacturing. This feature distinguishes FPGAs from Application Specific Integrated Circuits (ASIC), which are custom manufactured for specific design tasks. Although one-time programmable (OTP) FPGAs are available, the dominant types are SRAM based which can be reprogammed as the design evolves. They are referred to as 'field programmable' because they provide customers the ability to reconfigure the hardware to meet specific use case requirements after the manufacturing process. This allows for features upgrades and bug fixes to be solved in situ which is especially useful for remote deployment. Full SoC designs containing multiple processes can be put onto a single FPGA device.

FPGAs consist of many logic blocks, each typically consisting of flip-flops and logic functions and a routing network connecting the logic blocks. With FPGAs, you can redefine each logic block and the connections between connections that can be used to build complex digital logic ciruits without physically connecting individual gates and flip-flops.

### The flexibility of FPGAs

### How does FPGA programming work?

### How are FPGAs buildable using transistors?

### How are integrated circuits really just collections of transistors?

## Emulation and its advantages

## Extra reading
### Batteries
When a device is connected to a battery, a reaction called a _electrochecmical reation_ occurs that produces electrical energy. Batteries have two terminals, a positive (marked +) and a negative (marked -). If you wire a connection between the two terminals, the electrons will flow from the negative end to the positive end in the quickest possible way. This will quickly wear out the battery and is dangerous. To properly harness the electrical power produced by a battery you must connect it to a load. The load might be something like a light bulb or a radio. The internals of a battery is typically encased in a metal or plastic case. Inside the case is a cathode, which connects to the positive terminal and the anode which connects to the negative terminal. These components, more generally known as electrodes, occupy most of the space in a battery and are the place where electrical reactions occur. A seperator creates a barrier between the cathode and the anode, preventing the electrodes from touching while allowing electrical charge to flow freely between them. The medium that allows the electric charge to flow between the cathode and the anode is known as the electrolyte. Finally, the collector conducts the charge to the outside of the battery and through the load.
### Electrode
- An electrical conductor used to make contact with a nonmetallic part of a circuit
### Cathode
- An electrode where a reduction reaction occurs (gain of electrons for the electroactive species)
### Anode
- An electrode where an oxidation reaction occurs (loss of electrons for the electroactive species)
### Oxidation
- An oxidation reaction is an electrochemical reaction that produces electrons.
## References
- Transistors: https://www.youtube.com/watch?v=J4oO7PT_nzQ
- Transistors: https://builtin.com/hardware/transistor
- Electrode: https://en.wikipedia.org/wiki/Electrode
- Resistors: https://eepower.com/resistor-guide/resistor-fundamentals/what-is-a-resistor/#
- Resistors/ohms law: https://learn.sparkfun.com/tutorials/voltage-current-resistance-and-ohms-law/all
- Gates: https://en.wikipedia.org/wiki/AND_gate
- Gates: https://en.wikipedia.org/wiki/OR_gate
- Gates: https://en.wikipedia.org/wiki/Inverter_(logic_gate)
- Gates: https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:computers/xcae6f4a7ff015e7d:logic-gates-and-circuits/a/logic-gates
- Gates: https://en.wikipedia.org/wiki/NAND_gate
- Gates: https://logic.ly/lessons/xor-gate/
- Gates: https://en.wikipedia.org/wiki/XOR_gate
- Flip-flops: https://www.geeksforgeeks.org/flip-flop-types-their-conversion-and-applications/
- Batteries: https://electronics.howstuffworks.com/everyday-tech/battery.htm
- Capacitors: https://electronics.howstuffworks.com/capacitor.htm
- FPGAs: https://ebics.net/how-fpgas-work/
- FPGAs: https://www.arm.com/glossary/fpga
- FPGAs: https://www.xilinx.com/products/silicon-devices/fpga/what-is-an-fpga.html
- IC: https://learn.sparkfun.com/tutorials/integrated-circuits/all
