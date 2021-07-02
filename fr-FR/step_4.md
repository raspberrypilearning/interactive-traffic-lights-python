## Feux de circulation

Tu peux utiliser la classe `TrafficLights` intégrée plutôt que trois LEDs individuelles.

\--- task \---

Modifie la ligne `from gpiozero import...` pour remplacer `LED` par `TrafficLights`:

```python
from gpiozero import TrafficLights, Button
from time import sleep

bouton = Button(21)
lumieres = TrafficLights(25, 28, 27)

while True:
    bouton.wait_for_press()
    lumieres.on()
    bouton.wait_for_release()
    lumieres.off()
```

\--- /task \---

\--- task \---

Essaie de faire passer les lumières en `mode clignotement`:

```python
while True:
    lumieres.blink()
    bouton.wait_for_press()
    lumieres.off()
    bouton.wait_for_release()
```

\--- /task \---