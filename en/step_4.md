## Add button and pressed

--- task ---
add button to breadboard
![Push button in a breadbaord](images/button-full.png){:width="500px"}
--- /task ---

--- task ---
make the stepper thing into a function

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 6-9
---
from picozero import Pot
from time import sleep

sensor = Pot(26)  # Soil probe input

while True:  
    reading = sensor.value  
    print("Soil moisture:", round(reading, 2))  
    sleep(1)
--- /code ---

--- /task ---


--- task ---
call the function on button

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 6-9
---
from picozero import Pot
from time import sleep

sensor = Pot(26)  # Soil probe input

while True:  
    reading = sensor.value  
    print("Soil moisture:", round(reading, 2))  
    sleep(1)
--- /code ---

--- /task ---

--- task ---
Test
--- /task ---
