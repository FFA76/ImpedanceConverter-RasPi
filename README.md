# Instructions for building an Impedance converter for the Raspberry Pi

## Summary 

This project provides instructions for building an impedance converter for the [Raspberry Pi](https://www.raspberrypi.com/) (a single-board computer), as used in physics labs for students at the faculty of physics at the Karlsruhe Institute of Technology.

*Fig. 1*: Illustration of the impedance converter with measuring case used in the “photoelectric effect”-lab experiment.  
                    ![Figure 1](docs/images/Measuring_Case.png)

The framework for this is based on the [PhyPiDAQ](https://github.com/PhyPiDAQ) project by [Prof. Dr. Günter Quast](https://www.physik.kit.edu/personen_268.php), which aims to provide access to state-of-the-art measurement technology and data acquisition tools to students.

In the physics lab at KIT, the charging curve of a capacitor is measured and digitized, whereby the capacitor is charged by the current of a photocell.
The voltage difference across the capacitor be passed on to the ADC, without discharging the capacitor, via the high-impedance input and low-impedance output of the operational amplifier.

#### Currently available Documentation

- [Build instructions for circuit board](docs/Hardware_instructions.md)
- [Software instructions for Data acquisition](docs/Software_instructions.md)
