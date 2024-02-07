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
![NPN ciruit diagram]([https://github.com/NathanBlackburnDev/transistors/](https://github.com/NathanBlackburnDev/transistors/blob/main/images/NPN.png)https://github.com/NathanBlackburnDev/transistors/blob/main/images/NPN.png)
