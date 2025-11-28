## Challenge - randomly select

Edit your code to randomly select one of four options each time you press the button.


--- task ---
Add the `random` libraries and import the choice function.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 3
---
from picozero import Pot, Button, DigitalLED
from time import sleep
from random import choice

#define pins
stepper = Stepper((18, 19, 20, 21))
button = Button(15)
led = DigitalLED(14)

while True:
    if button.is_pressed:
        led.blink(0.3,0.3)
        #rotate motor
        stepper.rotate(90, 'cw')
--- /code ---

--- /task ---

--- task ---
The wheel has three angles to turn to: 90 degrees, 180 degrees, 270 degrees. 

Add an `angle` variable. Use `choice` to randomly choose between the three angles.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 14-15
---
from picozero import Pot, Button, DigitalLED
from time import sleep
from random import choice

#define pins
stepper = Stepper((18, 19, 20, 21))
button = Button(15)
led = DigitalLED(14)

while True:
    if button.is_pressed:
        led.blink(0.3,0.3)
        #rotate motor
        angle = choice([90, 180, 270])
        stepper.rotate(90, 'cw')
--- /code ---

--- /task ---

--- task ---
In the `stepper.rotate` function, replace the 90 degrees with `angle`.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 15
line_highlights: 15
---
        stepper.rotate(angle, 'cw')
--- /code ---

--- /task ---


--- task ---
There are two directions the wheel could turn: clockwise and counter clockwise.

Add a `direction` variable. Use `choice` to randomly choose between the two directions.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 16
---
from picozero import Pot, Button, DigitalLED
from time import sleep
from random import choice

#define pins
stepper = Stepper((18, 19, 20, 21))
button = Button(15)
led = DigitalLED(14)

while True:
    if button.is_pressed:
        led.blink(0.3,0.3)
        #rotate motor
        angle = choice([90, 180, 270])
        direction = choice(['cw','ccw'])
        stepper.rotate(angle, 'cw')
--- /code ---

--- /task ---

--- task ---
In the `stepper.rotate` function, replace the 'cw' with `direction`.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 17
line_highlights: 17
---
        stepper.rotate(angle, direction)
--- /code ---

--- /task ---

--- task ---
**Test:** Press the button and watch the wheel randomly turn a different angle or direction while the LED blinks.
--- /task ---


