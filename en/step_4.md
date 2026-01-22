## Add a button

--- task ---
Add a button to the breadboard. 

Connect one side of the button to **GND**. Connect the other side to **GP16**.

![The button sits across the gap in the middle of the breadboard, and wires connect the button to the Raspberry Pi Pico in the breadboard as described.](images/button-full.png){:width="500px"}
--- /task ---

--- task ---
Import `Button` from the `picozero` library.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 1
---
from picozero import Stepper, Button

# define the pins
stepper = Stepper((18, 19, 20, 21))

# turn the motor
stepper.turn(90, 'cw')
--- /code ---

--- /task ---


--- task ---
Define the button pin.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 5
---
from picozero import Stepper, Button

# define the pins
stepper = Stepper((18, 19, 20, 21))
button = Button(16)

# turn the motor
stepper.turn(90, 'cw')
--- /code ---

--- /task ---


--- task ---
Add code to turn the motor if the button is pressed. 

**Tip:** Look at how the code is indented now. This is important in Python.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 7-10
---
from picozero import Stepper, Button

# define the pins
stepper = Stepper((18, 19, 20, 21))
button = Button(16)

while True:
    if button.is_pressed:
        # turn the motor
        stepper.turn(90, 'cw')
--- /code ---

--- /task ---


--- task ---
**Test:** Press the button. Does the motor turn? 
--- /task ---
