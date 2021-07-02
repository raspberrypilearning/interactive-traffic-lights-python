## Semaforo

È possibile utilizzare la classe `TrafficLights` integrata anziché tre singoli LED.

\--- task \---

Modifica la riga `from gpiozero import...` sostituendo `LED` con `TrafficLights`:

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

Prova a modificare il comportamento delle luci con `blink`:

```python
while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
```

\--- /task \---