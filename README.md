# Theory of transistors, about FPGAs and ICs
This README contnet is from week 1 of [from the transistor by geohot](https://github.com/geohot/fromthetransistor). It talks about transistors, FPGAs, ICs and the electrical components/concepts needed to understand the content.
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
IC is a collection of electronic components such as resistors, transistors, capacitors etc. all stuffed into a tiny chip and connected together to achieve a common goal. They come in different flavours such as single-circuit logic gates, microcontrollers, microprocessors, FPGAs. The inside of an IC is a layering of semiconductor wafers, copper and other materials, which interconnect to form transistors, resistors, or other componenets in a circuit. The cut and formed combination of these wafers is called a die.

![Screen Shot 2024-02-10 at 09 13 22 am](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/5db5af14-64f3-498a-8d4c-b16a35adcafb)

The IC itself is tiny, the wafers of semiconductor and layers of copper it consists of are incredibly thin. The connections between the layers are very intricate.

![Screen Shot 2024-02-10 at 09 14 53 am](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/ddbfacdc-a6ca-4d73-a907-f1e2e7185116)

An IC die is the circuit in its smallest possible form, too small to solder or connect. To make it easier to connect to the IC, the die is packaged. The IC package turns the tiny die into the black chip you are indoubitably familiar with.

### IC packages
The package is what encapsulates the IC die and splays it out into a device we can more easily connect to. Each outer connection on the die is connected via a tiny piece of gold wire to a pad or pin on the package. Pins are the silver, extruding terminals on an IC, which go on to connect to other parts of a circuit. These are extremly important because they are what go on to connect to the rest of the componenets and wires in a circuit. There are many different types of packages, each of which has unique dimensions, mounting-types and pin counts.

![Screen Shot 2024-02-10 at 09 25 41 am](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/094780e0-7718-4bae-b73f-991bd0561264)

### Logic gates, Timers, Shift registers etc.
Logic gates can be packaged into their own integrated circuit. Some logic gate ICs might contain a handful of gates in one package, like this quad input AND gate:

![Screen Shot 2024-02-10 at 09 28 06 am](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/00cd91e6-dce7-4ff4-ae95-f9362db0703a)

Logic gates can be connected inside an IC to create timers, counters, latches (sort of similar to flip-flops), shift registers, and other basic logic circuitry.
### Microcontrollers, Microprocessors, FPGAs etc.
Microcontrollers, Microprocessors and FPGAs are all packing millions and billions of transistors into a tiny chip, they are all ICs. These components exist in a wide range of functionality, complexity and size; from an 8 bit microcontroller like the [ATmega32](https://www.microchip.com/en-us/product/atmega32) in an [Arduino](https://www.arduino.cc/), to a complex 64 bit, multi core processor organizing everything in your computer. 
### Resistors
The resistor is a passive electrical component that creates resistance in the flow of electric current. They are used in almost all electrical networks and electronic circuits. The resistance is measured in ohms (Ω). Electrical flow will pass through the resistor and the resistor will restrict the flow of the electric current. You can think of it like water flowing through a wide pipe, if the pipe at some point becomes very short the the resistance of the flowing water increases and thus less water comes through, the same applies here.

![Screen Shot 2024-02-09 at 16 57 30 pm](https://github.com/NathanBlackburnDev/transistors-FPGAs-ICs/assets/116575260/120cc707-0f08-418e-95d2-1f3356bbbc19)

The voltages between two points is equal to the current between the two points * the voltage
### Capacitors
A capacitor is similar to a battery, with the main difference being a capacitor cannot produce new electrocs, it only stores them. That is the reason as to why a capacitor is called such, because it has the capacity to store energy. Inside a capacitor, the terminals connect to two metal plates seperated by a non-conducting substance, or dielectric.
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

### Configurable Logic Blocks (CLB)
A CLB is the basic repeating logic resource on an FPGA. When linked together by routing resources, the components in CLBs execute complex logic functions, implement memory functions and synchronize code on the FPGA. CLBs contain smaller componenets like flip-flops, look-up tables (LUTs), and multiplexers.
### Flip-flops
Flip-flop is a circuit that maintains a state until directed by input to change the state. A basic flip-flop can be constructed using four-NAND or four-NOR gates. Flip flop is popuarly known as the basic digital memory circuit. It has 2 states, 1 and 0. A flip-flop is a sequential circuit that consists of a bit. It is the smallest storage resource on the FPGA. Each flip-flop in a CLB is a binary register used to save logic states between clock cycles on an FPGA circuit.
### Look-up table (LUT)
A LUT is a collection of gates hardwired on the FPGA. An LUT stores a predefined list of outputs for every combination of inputs. LUTs provide a fast way to retrieve the output of a logic operation because possible results are stored and then referenced rather than calculated. The LUTs in a CLB can also implement FIFOs. In laymens terms, an LUT is a table that determines what the output is for any given inputs.

One of the features that make FPGA families differ from, each other is their logic resource. For example, each CLB of [Spartan-II FPGAs](https://docs.xilinx.com/v/u/en-US/ds001) is comprised of two slices, each with two LUTs. The [Spartan 6](https://docs.xilinx.com/v/u/en-US/ds001) has two slices with four LUTs each. Internally, LUTs comprise of 1-bit memory cells (hold either 1 or 0) and a set of multiplexers. One value among these SRAM bits will be available at the LUTs output depending on the values fed to the control lines of the multiplexers. The numbher of inputs available for a LUT detemine its size. In general, a LUT with _n_ inputs is seen to comprise of 2 ** n:1 multiplexer

![Screen Shot 2024-02-10 at 19 10 47 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/ce2e5263-f8f1-429d-9801-9f7f90fdb394)

The above shows a 2 input LUT comprising of 4 SRAM bits and a 4:1 Mux.
### Implementation of logic functions using LUT
FPGA makes use of its LUTs as a preliminary resource to implement any logical function. This is actually a two step process. At first, the output values for each combination of input varaibles constituting the boolen function (truth table) are stored in the SRAM cells of the LUT. After this, depending on the combination of input variables supplied by the user, the appropriate memory bit will appear at LUT's output pin. This is due to the fact that the user provided input bits act as the select lines for the multiplexers present inside the LUTs.

Suppose we want to realize a boolean function of four input variables A, B, C and D using a 4-input LUT. Here, let the output high only when any of the two input variables are one. The truth table corresponding to this is show below.

![Screen Shot 2024-02-10 at 19 29 14 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/3ace4d9e-230c-44df-80e8-a41619b64bec)

While realizing this function using an FPGA, A, B, C and D will be the inputs to the LUT. Next, the values of the output variable for each of their combination will be stored in the SRAM cells. Now, if ABCD = 0101 then the output of the LUT (column Y) will take the value of 1 as the content of the sixth memory cell makes it way to the output pin (shown by red line)

![Screen Shot 2024-02-10 at 19 36 39 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/14a1b6ab-658c-4347-af7a-2096834f63a5)

### Importance of LUTs
Assume we have to compute a function like output the first 1001 fibonnaci numbers, this process is computationally expensive and thus inefficent, especially since the range is large. Instead we can pre-compute the cosines for all the possible inputs within the range and store them in a LUT. After this, computing any of the first 1001 fibonnaci numbers would invole the action of fetching (not computing) the corresponding value from the look-up table. This would greatly reduce the run time and make it much more efficient. 

In addition, note that the SRAM cells of the LUTs are one of the important factors which contribute to the reconfigurability of the FPGAs. This is because the configuration bits consulting them can be changed each time the device is powered up, which in turn changes their functionality. For example, the LUT acting as an adder can be made to behave as a subtractor just by [change values stored in its SRAM cells](https://uweb.engr.arizona.edu/~rlysecky/courses/ece274-05f/lectures/lecture23.pdf). This is a bit like a double edged swordm as almost all LUT operations are prone to glitches.

### Multiplexers
A multiplexer (also called Mux) is another word for selector. It acts much like a railroad switch.

![Screen Shot 2024-02-10 at 17 45 14 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/2484469f-7374-4a1e-af31-5acf458f1d1f)  ![Screen Shot 2024-02-10 at 17 45 22 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/abe8cf82-56e6-4ecb-895f-826c5efb0d6c)

The picture above shows two possible source tracks that can be connected to a single destination track. The railroad switch controls via some external control which train gets to connect to the destination track. This exact same concept is used with a 2-1 Mux, whereby two inputs can connect to a single output. Multiplexers are used all the time in FPGAs in various sizes and configurations. The image above and to the right shows what a 2-1 Mux looks like symbolically. The inputs to the Mux are **A**, **B** and **sel**, the output is **out**. A and B are the data inputs that get selected to the output, sel is the control signal. Muxes can come in all possible combinations depending on your particular use case. Typically, some number of inputs are selected to a single output. However the reverse could be true and it would still be a Mux. A single input could be selected to any number of outputs. 
## What are FPGAs?
Field Programmable Gate Arrays (FPGAs) are semiconductor devices that are based around a matrix of configurable logic blocks (CLBs) connected via programmable interconnects that allow the designer to connect blocks and configure them to perform everything from simple logic gates to complex functions. FPGAs can be reprogrammed to desired application or functionality requirements after manufacturing. This feature distinguishes FPGAs from Application Specific Integrated Circuits (ASIC), which are custom manufactured for specific design tasks. Although one-time programmable (OTP) FPGAs are available, the dominant types are SRAM based which can be reprogammed as the design evolves. They are referred to as 'field programmable' because they provide customers the ability to reconfigure the hardware to meet specific use case requirements after the manufacturing process. This allows for features upgrades and bug fixes to be solved in situ which is especially useful for remote deployment. Full SoC designs containing multiple processes can be put onto a single FPGA device.

FPGAs consist of many logic blocks, each typically consisting of flip-flops and logic functions and a routing network connecting the logic blocks. With FPGAs, you can redefine each logic block and the connections between connections that can be used to build complex digital logic ciruits without physically connecting individual gates and flip-flops.

![Screen Shot 2024-02-10 at 18 12 07 pm](https://github.com/NathanBlackburnDev/fromthetransistor-week1/assets/116575260/4350bbad-400d-44a9-b2bd-f16b2cf2ae95)

- CLBs shown as blue boxes above are the resources of FGPA meant to implement logic functions. Each CLB is comprised of a set of slices which are further decomposable into a definite nuber of LUTs, flip-flops (FFs) and Muxes
- I/O blocks (IOBs) available at FPGA periphery facilitate external connections. These programmable blocks carry signals to or from an FPGA chip. The IOBs are the green rectangles on the edge, but still inside the FPGA
- Switch matrix (red lines) is an interconnecting wire-like arrangment within FPGA. These offer connectivity for the CLBs or provide dedicated low impendance, minimum delay paths

### How does FPGA programming work?
FPGA programming uses a HDL to manipulate circuits depending on what capabilites you want the device to have. The process is different from programming a CPU or GPU, since you aren't writing a program that will run sequentially. Instead, you are using a HDL to create circuits and physically change the hardware depending on what you want it to do. The process is similar to programming software in that you write code that is turned into a binary file and loaded onto the FPGA, but the outcome is that the HDL makes physical changes to the hardware, rather than strictly optimizng the device to run software. A program on an FPGA pieces together lower-level elements like logic gates and memory blocks, which work in concert to complete a task. Because you're manipulating the hardware from the ground up, FPGAs allow a great deal of flexibility. You can adjust basic functions such as memory or power usage depending on the task.

### How are FPGAs buildable using transistors? How are they just a package of transistors?
FPGAs are an array of reconfigurable gates. They are built as an array of CLBs. Each CLB can be configured to perform combinational or sequential functions. 

As mentioned briefly above, FPGAs are really just a nice little collection of millions and even billions of transistors that come together to form an IC, of which an FPGA is a type of IC. Of course there will be other components but the transistor is arguably the most important one. Transistors can be used to build logic gates which enable you to perform basic logical operations. They can also be used as resistors and amplifiers. Metal-oxide-semiconductor (MOS) transistors can be used as memory cell storage elements, as well transistors can store 1 bit of information, so those billions of transistors inside the FPGA can be used to store 1 bit of information each, be used to perform logical operations by forming gates that take an input and result in a logical output, control the flow of electrons through the circuit, all of which when combined form the FPGA. FPGAs are esentially an array of reconfigurable gates. They are built as an array of CLBs, whereby each CLB can be configured to perfrom combinational or sequential functions. CLBs can be built with transistors by grouping together transistors to form a CLB. This just means that FPGAs and any IC really can be built just with transistors, as the transistors come together to form logic gates used to perform logical operations, CLBs used to perform complex functions, store memory, and enable communication between all electrical componenets.

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
- An oxidation reaction is an electrochemical reaction that produces electrons
### SRAM and DRAM
- There are two types of RAM: Static access random memory and Dynamic access random memory
- With DRAM, the bits are stored in cells that consist of one capacitor and one transistor. So due to capacitor leakage, DRAM needs to be refreshed often. Therefore, DRAM is 10x slower than SRAM. The average access time of DRAM is about 60 nanoseconds, while SRAM can give access times as low as 8 nano seconds. SRAM is faster and typically used for cache. DRAM is less expensive and has a higher density and has a primary use as a main processor memory/cache. With SRAM, each cell consists of six transistors and can store one single bit.
### FPGA slices
- Hardware resources on an FPGA are indicated by the number of slices that FPGA has, where a slice is comprised of LUTs and FFs
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
- CLB: https://www.ni.com/docs/en-US/bundle/labview-nxg-fpga-targets/page/configurable-logic-blocks.html
- Flip-flops: https://www.geeksforgeeks.org/flip-flop-types-their-conversion-and-applications/
- Batteries: https://electronics.howstuffworks.com/everyday-tech/battery.htm
- Capacitors: https://electronics.howstuffworks.com/capacitor.htm
- Multiplexer: https://nandland.com/multiplexer-mux/
- FPGAs: https://ebics.net/how-fpgas-work/
- FPGAs: https://www.arm.com/glossary/fpga
- FPGAs: https://learn.sparkfun.com/tutorials/how-does-an-fpga-work/all
- FPGA + CLB: https://www.sciencedirect.com/topics/computer-science/configurable-logic-block
- FPGAs: https://www.xilinx.com/products/silicon-devices/fpga/what-is-an-fpga.html
- FPGA programming: https://www.xilinx.com/products/silicon-devices/resources/programming-an-fpga-an-introduction-to-how-it-works.html
- FPGA programming: https://www.xilinx.com/products/silicon-devices/resources/programming-an-fpga-an-introduction-to-how-it-works.html
- IC: https://learn.sparkfun.com/tutorials/integrated-circuits/all
- SRAM: https://en.wikipedia.org/wiki/Static_random-access_memory
- SRAM cells: https://www.hackster.io/salvador-canas/a-practical-introduction-to-sram-memories-using-an-fpga-i-3f3992
- FPGA slices: https://www.ni.com/en/support/documentation/supplemental/18/slices-on-an-fpga-chip.html
- LUTs: https://www.allaboutcircuits.com/technical-articles/purpose-and-internal-functionality-of-fpga-look-up-tables/
