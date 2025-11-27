## Challange - random angle choice

--- task ---
carefully move the dial (and stepper motor) so that it is over one of the words
![Animated gif of moving the dial into the right place](images/IMAGE.png)
--- /task ---

--- task ---
add libraries

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
add rand and choce in function

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
change the methods in the stepepr.rotate

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
test
--- /task ---


