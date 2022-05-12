# PiDP-11 ChasingLEDs
ChasingLEDs - a configurable blinkenlight idle system for the PiDP-11

Learning a bit of bare-metal assembly language on the PiDP-11, and this is what I ended up with: the well known LED's chasing each other from left ro right and back in the Data Register Display. However, I made it configureable, both with regards to the LED pattern and the speed.

Switches 0 to 14 mimic the LED pattern moving to the left and right. The pattern changes according to the set switches the moment a new cycle (LED's start to move to the left) begins.

When Switch 15 is set, the other switches set the delay of the LED's moving (not really visible as long as switch 15 is set). The higher the octal number set by the switches, the slower (more delay) the LED's will move. With switch 15 turned off again, the speed changes the moment the LED's have moved. Therefore, restrain from entering a very high number, or you will be waiting a long time before a new and more reasonable speed takes effect.

Because the pattern will change when adjusting the speed, it is best to first set an appropriate speed and then the pattern. But you can play around with the switches as you like!

The boot.ini file has a similar intro as the default idled has, should you want to use it as option 0000 in the selections file, for instance.
