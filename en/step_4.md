## Add a button

--- task ---
Add a button to the breadboard. 

Connect one side of the button to GND.
Connect the other side to GP16.

![Push button in a breadbaord](images/button-full.png){:width="500px"}
--- /task ---

--- task ---
Import Button from the picozero library.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 1
---
from picozero import Stepper, Button

#define pins
stepper = Stepper((18, 19, 20, 21))

#rotate motor
stepper.rotate(90, 'cw')
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

#define pins
stepper = Stepper((18, 19, 20, 21))
button = Button(16)

#turn motor
stepper.turn(90, 'cw')
--- /code ---

--- /task ---


--- task ---
Add code to turn the motor if the button is pressed.

**Tip:** Look how the code is now indented, this is important with python.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 7-10
---
from picozero import Stepper, Button

#define pins
stepper = Stepper((18, 19, 20, 21))
button = Button(16)

while True:
    if button.is_pressed:
        #turn motor
        stepper.turn(90, 'cw')
--- /code ---

--- /task ---


--- task ---
**Test:** Press the button. Does the motor turn? 
--- /task ---
