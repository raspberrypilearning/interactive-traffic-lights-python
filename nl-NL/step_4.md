## Verkeerslichten

Je kunt de ingebouwde `TrafficLights` klasse gebruiken in plaats van drie losse LED's.

--- task ---

Vervang in de `from gpiozero import...` regel de `LED` met `TrafficLights`:

```python
from gpiozero import TrafficLights, Button
from time import sleep

button = Button(21)
lights = TrafficLights(25, 28, 27)

while True:
    button.wait_for_press()
    lights.on()
    button.wait_for_release()
    lights.off()
```

--- /task ---

--- task ---

Probeer de lichten te veranderen naar `blink` (knipperen):

```python
while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
```

--- /task ---