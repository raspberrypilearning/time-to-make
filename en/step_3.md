## Turn it

--- task ---

Open a **new file** in the [Thonny IDE](http://thonny.org/){:target="_blank"}. 

If you need help getting your Raspberry Pi Pico up and running, check out our [Getting Started with Pico Guide](https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/2){:target="_blank"}

--- /task ---

--- task ---
Add the `time` and `picozero` libraries and import the Stepper and sleep functions.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 1
---
from picozero import Stepper
--- /code ---

--- /task ---


--- task ---
Define the stepper motor pins.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 3-4
---
from picozero import Stepper

#define pins
stepper = Stepper((18, 19, 20, 21))
--- /code ---

--- /task ---


--- task ---
Test the motor by moving it 90 degrees clockwise. This is shortened to `cw`.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 6-7
---
from picozero import Stepper

#define pins
stepper = Stepper((18, 19, 20, 21))

#turn motor
stepper.turn(90, 'cw')
--- /code ---

--- /task ---


--- task ---
**Test:** watch the motor turn when you run the code.
--- /task ---

