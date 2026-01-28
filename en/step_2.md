## Wire the motor

--- task ---

Insert your Raspberry Pi Pico into the breadboard.
![The Raspberry Pi Pico on a breadboard, positioned across the gap in the middle.](images/pico.png){:width="300px"}

--- /task ---

--- task ---

Insert the stepper motor wires into the driver.

**Tip:** Drivers vary. If your driver looks different to this, skip the rest of this step and look up where the wires go for your specific driver.

![A diagram of the stepper motor connected to the driver board.](images/driver.png){:width="300px"}

--- /task ---


--- task ---

To power the driver, first, add a wire from **+** on the driver to **VBUS** on the Raspberry Pi Pico. 

Then, add a wire from **-** on the driver to **GND** on the Raspberry Pi Pico.

![Wires connect + and - on the driver with the VBUS and GND pins on the Raspberry Pi Pico in the breadboard.](images/power-full.png){:width="500px"}

--- /task ---


--- task ---

Add wires to connect the pins of the driver to the Raspberry Pi Pico:
- Driver pin **1** to **GP18**
- Driver pin **2** to **GP19**
- Driver pin **3** to **GP20** 
- Driver pin **4** to **GP21**

![Wires connect the driver pins to the pins of the Raspberry Pi Pico in the breadboard as described.](images/driver-full.png){:width="500px"}

--- /task ---