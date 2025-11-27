## Add LEDs

--- task ---
add leds
![LEDs in a breadbaord](images/led-full.png){:width="500px"}
--- /task ---

--- task ---
make a flashy function

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
add to call when button pressed

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


