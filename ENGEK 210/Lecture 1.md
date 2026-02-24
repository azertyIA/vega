The five steps in the engineering design process are:
1. Problem Definition: speak with the client to find out what you have to build. 
2. Conceptual Design: a bunch of sensor -> actuator concepts
3. Preliminary Design: put together the concepts to one big design
4. Detailed Design: refine refine refine
5. Communication: show to class

### Product Definition
The goal is to:
- create an accurate problem statement
- determine objectives (attributes), metrics (assessments), and constraints
- begin thinking about the black box functions and the means (<$200)

One example of a problem statement:
> We wish to design a device to measure the temperature of everyone walking through the front door of the Boston Medical Center as a preliminary indicator of either COVID-19 or the flu.

The main objective for this should be:
- Measure non-contact forehead temperature
- provide an alarm for high temperature
- easy to clean
- be reliable
- be accurate + precise
- be safe, affordable, fast, portable

> The difference between accuracy and precision is mean vs spread.

The resulting metrics then should be:
- how far away you are
- how loud it is when the temperatures are high
- time to clean????????
- how many times before it breaks
- lumens of the screen

To determine the ordering of the objectives just ask your teammates.

## Glass Box
The box that happens before the glass box is actually the black box. There is some information and energy going into the box and its giving some kind of output (information or energy). For the example of the flashlight however, the inputs would be whether the button is clicked as information and a battery as energy. Its outputs should be energy as light. And then you say what processes go on inside the box.

Functional analysis aspects include:
- accepting/supplying power
- trigger sensing
- temperature sensing (all comes out as either charge or current)
- send signal to processor
- convert signal to useful information (calibration)
- determine if its in the range of interest
- sound alarm
- display temperature
- hold components

