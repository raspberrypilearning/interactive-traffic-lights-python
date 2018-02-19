## Traffic lights

You can use the built-in `TrafficLights` interface instead of three LEDs.

1. Amend the `from gpiozero import...` line to replace `LED` with `TrafficLights`:
    
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

2. Try changing the lights to `blink`:
    
    ```python
while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
```