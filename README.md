# Heart-Shaped-LED-PCB
A PCB that has LEDs shaped in the form of a heart and uses an 8 bit shift register SN74HC595DR to make patterns on the LEDs

# Introduction
I decided to embark on this project as a way to get started in PCB design and soldering. I had a Freenove kit lying around with a shift register and some LEDs and I thought making a pattern with them would be very cool. I also thought it would be a good present for Valentine's day.

# Component and Materials
- SN74HC595NSR - 8 bit shift register
- Eight LEDs (4 red, 4 white)
- One 220 Ω Resistor
- Three Push Buttons - PTS526SK15SMTR2 LFS
- Three 10.5 kΩ Resistors (Pull Down Resistors)
- One Battery Holder (BS-7)
- One 20mm Coin 3V Battery

# Circuit Design
![alt text](https://github.com/h0nt3d/Heart-Shaped-LED-PCB/blob/main/images/schematic-1.png?raw=true)
Fig 0.0 - Schematic of the Circuit

Operation:
- Place the battery into the battery holder.
- The 3 push buttons are connected to, Serial, SRCLK (Serial Clock) and RCLCK (Register ClCK).
- To load a bit, hold Serial and SRCLK together.
- To display a shift of the loaded bit press RCLK
- To shift the bit again without another load in, Press SRCLK then press RCLK.

Behaviour of components:
- Each output from the register is connected to an LED that lights up indicating that a bit is being stored.
- Active low Clear of register is connected to ground to prevent reset.
- 200 Ω Limiting resistor used to protect LEDs from excessive current flow.
- 10.5 kΩ connected to a push button each acting as pull down resistors to prevent impedance state.

# Footprint View & 3D View
![alt text](https://github.com/h0nt3d/Heart-Shaped-LED-PCB/blob/main/images/footprintEditor.png?raw=true)
Fig 1.0 - Footprint View View of PCB

![alt text](https://github.com/h0nt3d/Heart-Shaped-LED-PCB/blob/main/images/3D.png?raw=true)
Fig 1.1 - 3D View of PCB


# Observations & Improvements
- Signs of Impedance are present indicating a faulty connection of pull down resistors.
Improvement: Use a larger resistor or THT resistor to increase ease of soldering.
- The use of one 200 Ω resistor lead to uneven lighting between LEDs. Improvement: Connect each LED to its own resistor.

# Conclusion
- From this mini project, I learned some of the pros and cons of using SMD components and THT components. It also gave me more experience in handling a soldering iron and taught me the process of using gerber files to order PCBs from a manufacturer.

# Future Enhancements
- Implementation of a binary counter using a 555 timer.
- Implementation with a microcontroller e.g. Arduino, Freenove Board
