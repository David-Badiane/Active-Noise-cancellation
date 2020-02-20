# Active noise cancellation headsets

Noise cancelling headphones are an ideal choice for many music listeners for their ability to cut out ambient noise without raising the audio volume to levels that might be dangerous for the ear. Even with no music playing, the headphones have the ability to mute ambient noise – perfect for those trying to work or sleep in noisy environments as airplanes, factories, etc.

Noise cancellation can be achieved in many modes, from **DSP** to **analog circuitry**.

In this small presentation we will discuss about an analog circuit able to reduce noise targetting certain frequencies.

[main circuit](https://www.partsim.com/simulator#266711)

<p align ="center" > <img width =700" height ="400" src = "/schematic.png"> </p>
<p align ="center" > <img width ="900" height ="600" src = "/circuit.jpg"> </p>

For each channel we have a:

**MICROPHONE SETTING STAGE**

**MICROPHONE PREAMPLIFICATION STAGE**

**ALLPASS CIRCUIT for delaying and timing**

**INVERTING ADDER**

**SPEAKER**

## Microphone setting stage

I employed an omnidirectional microphone of series number 14/00148-00.
Sensibility:-44±2 dB
Impedance:<2,2 KOHM
voltage-supply:3 V

Since the voltage needed is inferior to the supplied one, i created a Resistive bridge that gives me the needed voltage.

<p align ="center" > <img width =700" height ="400" src = "/schematic0.png"> </p>
  
## Microphone inverting preamp

The chosen opamp are ST-LF356N, some Jfet input Opamps carachterised by low harmonic distortion, low V-offset, wide band.
The first stage is a classic inverting amplifier.

<p align ="center" > <img width =700" height ="400" src = "/schematic1.png"> </p>

## Allpass delaying circuit

This stage is necessary to adjust the timing, the idea of the project was to employ two microphones, but I missed big electrolitic capacitors, and the jack entry plug was just one for both the channels. So i calculated the time delay from putting the microphone in the upper-middle side of the headphones, in a symmetrical fashion. 
The distance between ears and microphone is more or less of 14cm. tuning the noise cancellation at the fequency of 1kHz:

<p align ="center" > <img width =700" height ="400" src = "/schematic2.png"> </p>

## Adder and speaker output

<p align ="center" > <img width =700" height ="400" src = "/schematic3.png"> </p>
  
# PROBLEMS

1) It isn't easy to fecth the audio signal from the jack cable, I tried cutting and rewiring the jack cable but it resulted damagesd,  so i then tried to work directly with the signal, but again it's not easy to fetch the audiosignal from the speakers via wires for the noise and for finding the means to do it. I made another cable from the previous headphones I destroyed, but it seems to not work. 
2)I have problems in activating the microphone
3) I used Arduino oscilloscope and found out that the cable that takes the music does not work, and that the microphone isn't working either. Opamps seem to be working.
4) the wires of the microphone and the breadboard fetch a lot of noise, isolation is strictly necessary.

<p align ="center" > <img width =400" height ="600" src = "/final state.jpg"> </p>
## Simulation



**thanks for your attention**
