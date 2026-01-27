## Add an LED

--- task ---

Add an LED and a 220Ω resistor to the breadboard:

- Put one leg of the resistor into **GP15** in the Raspberry Pi Pico, and the other into a free row in the breadboard
- Add a socket-to-pin wire from the long leg of the LED to the row where you have just added the second leg of the resistor
- Add a socket-to-pin wire from the short leg of the LED to **GND**

![The resistor has been inserted into the breadboard and the LED is connected to the breadboard with wires as described.](images/led-full.png){:width="500px"}

--- /task ---

--- task ---

Import `LED` from the `picozero` library.

--- code ---

---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 1
---
from picozero import Stepper, Button, LED

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

Define the pin for the LED.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 6
---
from picozero import Stepper, Button, LED

# define the pins
stepper = Stepper((18, 19, 20, 21))
button = Button(16)
led = LED(15)

while True:
    if button.is_pressed:
        # turn the motor
        stepper.turn(90, 'cw')
--- /code ---

--- /task ---

--- task ---

Make the LED blink. 

To experiment with the length of time that the LED is on and off, change the numbers in the brackets. The first number sets how long the LED is on, and the second number sets how long it is off.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 10
---
from picozero import Stepper, Button, LED

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

**Test:** Does the LED blink when you push the button?

--- /task ---


