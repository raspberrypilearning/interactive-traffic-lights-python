## Közlekedési lámpa

Használhatod a beépített `TrafficLights` osztályt a három különálló LED helyett.

\--- task \---

Írd át a `from gpiozero import...` sort, cseréld ki a `LED`-et `TrafficLights`-ra:

```python
from gpiozero import TrafficLights, Button
from time import sleep

gomb = Button(21)
lampak = TrafficLights(25, 28, 27)

while True:
    gomb.wait_for_press()
    lampak.on()
    gomb.wait_for_release()
    lampak.off()
```

\--- /task \---

\--- task \---

Próbáld meg megváltoztatni a lámpákat, hogy `villogjanak`:

```python
while True:
    lampak.blink()
    gomb.wait_for_press()
    lampak.off()
    gomb.wait_for_release()
```

\--- /task \---