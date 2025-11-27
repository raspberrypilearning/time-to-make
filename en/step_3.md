## Make it turn

If you need help getting your Raspberry Pi Pico up and running, check out our [Getting Started with Pico Guide](https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/2){:target="_blank"}

--- task ---
Open a **new file** in your code editor.
--- /task ---

--- task ---
Add the `time` and `picozero` libraries and import the Stepper and sleep functions.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 1-2
---
from picozero import Stepper
from time import sleep
--- /code ---

--- /task ---


--- task ---
Define t
18 19 20 21

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 4-5
---
from picozero import Stepper
from time import sleep

#define pins
stepper = Stepper((18, 19, 20, 21))
--- /code ---

--- /task ---


--- task ---
Test the motor by get code stepper to move 90 degrees clockwise. This is shortened to `cw`.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 7-8
---
from picozero import Stepper
from time import sleep

#define pins
stepper = Stepper((18, 19, 20, 21))

#rotate motor
stepper.rotate(90, 'cw')
--- /code ---

--- /task ---


--- task ---
**Test:** watch the motor turn when you run the code.
--- /task ---

