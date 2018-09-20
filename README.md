# OEP3W-MD4103-Amplifier
Audio Amplifier Class D 3W module for Arduino (and others)

# See the associated YouTube video # 121 here https://www.youtube.com/ralphbacon  
(Direct link to video: https://youtu.be/W9GpPW-u71s)

This tiny audio amplifier, that runs from 3 volts to 5.5 volts caught my eye and thought it would be worth further investigation.

All it needs is a 3W 4ohm speaker and an input signal and you're good to go.  

**Connection details**  
Connect the IN- to ground.  
Connect the IN+ to your input signal.  
VCC to +ve (max 5.5 volts @ 500mA)  
GND to ground (or -ve)  
CS can be controlled via your µController, to switch off the amplifier and reduce its current to 0.1µA (typical).  You can do this by connecting CS to a GPIO and bringing that pin LOW to disable the amplifier. Bring it back HIGH to switch the amp on.  
SP+ and SP- to your speaker.  

You _may_ need to decouple your input signal via a 1µF capacitor; in this demo I didn't. Try it without first.

If you want a **volume control**, just connect a 10K potentiometer (or preset resistor) as follows:

Connect one end of the pot to your input signal  
Connect the slider(middle terminal) to IN+ on this module   
Connect the other end of the pot to ground  

As the demo shows, it provides a good volume but it will be MUCH better once mounted in an enclosure (eg, your project box) to prevent the sound waves from the rear of the speaker cancelling out the sound waves from the front (making it sound tinny and quiet).

Distortion is 10% at full (3W) power, dropping to just 1% at 2.5W power. Probably about the same as a hand-held transistor radio.

To understand why this Class D amplifier can deliver 3W without melting (or a heatsink) read the following articles:  
1. https://en.wikipedia.org/wiki/Power_amplifier_classes  
2. https://www.electronicdesign.com/analog/understanding-amplifier-operating-classes  

