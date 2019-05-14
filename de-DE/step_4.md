## Verkehrsampel

You can use the built-in `TrafficLights` class instead of three individual LEDs.

\--- task \---

Amend the `from gpiozero import...` line to replace `LED` with `TrafficLights`:

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

\--- /task \---

\--- task \---

Try changing the lights to `blink`:

```python
while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
```

\--- /task \---