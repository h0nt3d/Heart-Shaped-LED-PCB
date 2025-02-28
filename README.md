# `Heart-Shaped-LED-PCB`
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

Fig 1.1 - Schematic of the Circuit

Operation:
- Place the battery into the battery holder.
- The 3 push buttons are connected to, Serial, SRCLK (Serial Clock) and RCLCK (Register ClCK).
- To load a bit, hold Serial and SRCLK together.
- To display a shift of the loaded bit press RCLK
- To shift the bit again without another load in, Press SRCLK then press RCLK.
