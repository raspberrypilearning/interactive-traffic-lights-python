## Semafori

È possibile utilizzare l'interfaccia `TrafficLights` al posto dei tre LED.

button = Button(25) lights = TrafficLights(24, 23, 22)

while True: button.wait_for_press() lights.on() button.wait_for_release() lights.off()

```python
```python
from gpiozero import TrafficLights, Button
from time import sleep
```

\--- /task \---

\--- task \---

Modifica la riga `from gpiozero import...` sostituiendo `LED` con `TrafficLights`:

```python
Prova a modificare il comportamento delle luci con `blink`:

    ```python
while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
```

\--- /task \---