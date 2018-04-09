## Verkeerslichten

Je kunt de ingebouwde `TrafficLights` interface gebruiken in plaats van drie LED's.

1. Vervang in de `from gpiozero import...` regel de `LED` met `TrafficLights`:
    
    ```python
from gpiozero import TrafficLights, Button
from time import sleep

button = Button(25)
lights = TrafficLights(24, 23, 22)

while True:
    button.wait_for_press()
    lights.on()
    button.wait_for_release()
    lights.off()
```

2. Probeer de lichten te veranderen naar `blink` (knipperen):
    
    ```python
while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
```