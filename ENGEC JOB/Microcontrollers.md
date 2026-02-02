A typical device has a microcontroller with the same voltage as a 3.3 V or 5 V power supply that the microcontroller is powered by. You have a few options:
- Arduino Pro Micro ($7): 16 MHz for slow update rate. Uses C/C++.
- Raspberry Pi Pico ($5): 133 MHz with higher processing power. Uses Python.
- Conventional R. Pi ($15): 1 GHz for 3.3V laptop scenarios. Uses Linux.

Sensors come in two different flavors: digital (I2C, SPI) and analog (noisy). Use digital sensors if possible and make sure the voltage matches and provide clean power to sensors using capacitors.

Some inputs include:
- temperature (https://a.co/d/40u6opo)
- motion (https://a.co/d/48kAHNf)
- switches, knobs, rotary encoders, potentiometers

Some outputs include:
- single color and multi color LEDs (put a 330 Ohm Resistor)
- neopixels exist as address LEDs, and LED matrices require better CPUs
- LCDs could use only just 1-2 pins
- color graphics displays should only be used with conventional R. Pis
- OLED or LCD graphics can be done in 2-3 pins
- actuators need 10 mA which need a driver circuit (a MOSFET or four for an H-bridge)

For more precision:
- open loop motors (stepping motors) just have instructions
- closed loop motors (servo motors) have a position feedback system

For connectors:
- 5.5 barrel jack is common for power up to 10 A
- XT connectors are much better than 3 pin connectors
- pin headers are good as well as screw terminals

For power:
- 4 batteries gets you 6 V
- portable USB-A chargers can get you 5 V
- power tool batteries are also always fun.
- rechargeable Li-Ion packs are compact and 3.7 V per cell.

For conversion:
- boost converters increase the voltage while buck converters decrease voltage