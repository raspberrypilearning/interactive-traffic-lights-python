## Control the LEDs and button

--- task ---

Open **Mu** from the main menu.

--- /task ---

--- task ---

Enter the following code:

```python
from gpiozero import LED, Button

red = LED(25)
button = Button(21)

while True:
    if button.is_pressed:
        red.on()
    else:
        red.off()
```

--- /task ---

--- task ---

Run your code with `F5`. Now when you press the button, the green LED will come on.

--- /task ---

--- task ---

Try creating three LEDs:

```python
from gpiozero import LED, Button

red = LED(25)
amber = LED(28)
green = LED(27)

button = Button(21)
```

--- /task ---

--- task ---

Get them to come on when the button is pressed:

```python
while True:
    if button.is_pressed:
        green.on()
        amber.on()
        red.on()
    else:
        green.off()
        amber.off()
        red.off()
```

--- /task ---

--- task ---

Run the code and press the button.

--- /task ---
