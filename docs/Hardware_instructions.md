# Build instructions for building an Impedance converter for the Raspberry Pi
The circuit board described below is based in part on that of the PhyPiDAQ-project's portbale [Measuring case](https://github.com/PhyPiDAQ/MeasuringCase).

*Abb. 1*: Circuit diagram of the impedance converter.  
                    ![Figure 1](images/Circuit_diagram.png)

A list of the electrical components and part numbers is available at [components](/docs/components).

The power supply for the measurement box is provided via the 5V pinout of the Raspberry Pi.
The 5. generation of RasPi's are used in the physics labs at the Faculty of Physics at KIT. To run the [PhyPiDAQ](https://github.com/PhyPiDAQ) software, it is recommended to use a RasPi from the 3. generation onwards.

A CA3140 chip is used as an operational amplifier under the use of a voltage follower, which receives a symmetrical supply voltage of 5V from a TMA-0505D. The preceding capacitors and resistors are used to stabilize the voltage.
