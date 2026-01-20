## Challenge: Turn randomly

Edit your code to randomly select one of the four options each time you press the button. This will make the selection wheel more fun to use!


--- task ---
Add the `random` library and import the `choice` function.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 2
---
from picozero import Stepper, Button, LED
from random import choice

# define the pins
stepper = Stepper((18, 19, 20, 21))
button = Button(16)
led = LED(15)

while True:
    if button.is_pressed:
        led.blink(0.3,0.3)
        # turn the motor
        stepper.turn(90, 'cw')
--- /code ---

--- /task ---

--- task ---
To get to one of the four text options on your selection wheel, the wheel has to turn to either 90 degrees, 180 degrees, 270 degrees, or 360 degrees.

Add an `angle` variable. Use `choice` to randomly choose between the four angles.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 13
---
from picozero import Stepper, Button, LED
from random import choice

# define the pins
stepper = Stepper((18, 19, 20, 21))
button = Button(16)
led = LED(15)

while True:
    if button.is_pressed:
        led.blink(0.3,0.3)
        # turn the motor
        angle = choice([90, 180, 270, 360])
        stepper.turn(90, 'cw')
--- /code ---

--- /task ---

--- task ---
In `stepper.turn()`, replace `90` (degrees) with `angle`.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 14
line_highlights: 14
---
        stepper.turn(angle, 'cw')
--- /code ---

--- /task ---


--- task ---
There are two directions the wheel could turn: clockwise and counterclockwise (anticlockwise).

Add a `direction` variable. Use `choice` to randomly choose between the two directions. 'Counterclockwise' is shortened to **'ccw'**.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 14
---
from picozero import Stepper, Button, LED
from random import choice

# define the pins
stepper = Stepper((18, 19, 20, 21))
button = Button(16)
led = LED(15)

while True:
    if button.is_pressed:
        led.blink(0.3,0.3)
        # turn the motor
        angle = choice([90, 180, 270, 360])
        direction = choice(['cw','ccw'])
        stepper.turn(angle, 'cw')
--- /code ---

--- /task ---

--- task ---
In `stepper.turn()`, replace `'cw'` with `direction`.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 15
line_highlights: 15
---
        stepper.turn(angle, direction)
--- /code ---

--- /task ---

--- task ---
**Test:** Press the button and watch the wheel randomly turn a different angle or direction while the LED blinks.
--- /task ---


