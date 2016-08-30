# Entropy in your pocket!

![](https://raw.githubusercontent.com/denkimono/noise-generator/master/noise-unit-display.jpg)

[![Noise generator demo](http://img.youtube.com/vi/ZSrrZK398-U/0.jpg)](https://www.youtube.com/watch?v=ZSrrZK398-U)

This is a random number generator but rather than using an algorithm to create only pseudo-random numbers it uses the noise generated by billions of electrons smashing into silicon atoms. This noise is then processed to give a uniform distribution of numbers from 0 to 99 which appears on the display. In addition a speaker on the device enables the noise to be heard. By loading different software onto the device, the numbers can be sent to a computer via a serial link (TTL levels)

## How it works

The noise is generated by applying a reverse voltage to the base-emitter (P-N) junction of a transistor. Normally a P-N junction resists the flow of current in the reverse direction, but if the voltage is high enough then the electrons have enough energy to knock other electrons out of their silicon atoms. These electrons are themselves accelerated by the electric field and knock more electrons out. The process continues and the junction begins to conduct. This effect is called avalanche breakdown.

This generates random voltage fluctuations in the circuit which are amplified and sampled by the microcontroller. Although the noise forms a Gaussian-like distribution of sample values, the probability of an even sample is equal to the probability of an odd sample, so by taking the least significant bits of consecutive samples a flat (uniform) distribution of values can be obtained.

The device is designed to run off a PP3 9V battery (not included).

## How to build it

The file 'bom.txt' contains the parts list and a link to buy them (although these aren't the only sources of these components)

The folder 'gerber' contains all the CAD files you need to make the PCB - just send them off to your favourite board house!

The folder 'code' contains the software to be loaded on to the microcontroller. Type 'make' to build and 'make program' to load it onto the microcontroller using avrdude.

The file 'assembly-instructions.pdf' tells you how to put it together.


