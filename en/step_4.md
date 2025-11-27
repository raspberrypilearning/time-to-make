## Add a button

--- task ---
Add A button to the breadboard. 

Use a black wire from the button to GND (-18)
Use a purple wire from the other side of the button to GP16 (-20)

![Push button in a breadbaord](images/button-full.png){:width="500px"}
--- /task ---

--- task ---
Add to the code to rotate the motor if the button is pressed.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 7-8
---
from picozero import Pot
from time import sleep

#define pins
stepper = Stepper((18, 19, 20, 21))

while True:
    if button.is_pressed:
        #rotate motor
        stepper.rotate(90, 'cw')
--- /code ---

--- /task ---


--- task ---
**Test:** Press the button and watch the motor turn. 
--- /task ---
