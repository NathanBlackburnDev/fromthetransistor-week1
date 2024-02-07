# Theory of transistors, about FPGAs and ICs
This README talks about the theory of transistors, about FPGAs and how they are buildable using transistors and integrated circuits.
## What are transistors
Transistors are small electronic components with two main functions: switch circuits on or off and amplify signals. Small lower power transistors will be in a resin case but a higher power transistor will have a metal/resin case which is used to remove the heat from the transistor. Transistors have 3 pins, 1 is the emitter (E), 1 is the base (B) and the final one is the collector (C.). The emitter serves as the source of electrons, the base as the control terminal (essentially it controls the flow of electrons through the transistor) and collector which is the drain for the electrons. 
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

![NPN w current](https://github.com/NathanBlackburnDev/transistors/assets/116575260/277ef9ad-d7ce-41cd-8bcc-cb37ceb13adc) ![PNP w current](https://github.com/NathanBlackburnDev/transistors/assets/116575260/80db2f88-9588-4a3e-9a20-426a2c0009db)

On the top in the NPN, you can see the current (green arrows) flowing out of the negative side of the battery and inside the positive, but on the bottom in the PNP the opposite is happening where the current goes into the negative side and out the positive.
