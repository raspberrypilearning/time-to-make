## Turn the motor

--- task ---

Open a **new file** in [Thonny](http://thonny.org/){:target="_blank"}. 

If you need help getting ready to program your Raspberry Pi Pico, check out our ['Getting started with Raspberry Pi Pico' guide](https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/2){:target="_blank"}.

--- /task ---

--- task ---
Add the `picozero` library and import `Stepper`.

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
Define the pins for the stepper motor.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 3-4
---
from picozero import Stepper

# define the pins
stepper = Stepper((18, 19, 20, 21))
--- /code ---

--- /task ---


--- task ---
To test the motor, move it 90 degrees clockwise. 'Clockwise' is shortened to **'cw'**.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 6-7
---
from picozero import Stepper

# define the pins
stepper = Stepper((18, 19, 20, 21))

# turn the motor
stepper.turn(90, 'cw')
--- /code ---

--- /task ---


--- task ---
**Test:** Run the code and watch the motor turn.
--- /task ---

