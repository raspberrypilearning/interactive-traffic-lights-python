## Feux de circulation

Vous pouvez utiliser l'interface `TrafficLights` intégrée à la librairie gpiozero au lieu de trois DELs.

bouton = Button(25) feux = TrafficLights(24, 23, 22)

while True: bouton.wait_for_press() feux.on() bouton.wait_for_release() feux.on()

```python
```python
from gpiozero import TrafficLights, Button
from time import sleep
```

\--- /task \---

\--- task \---

Modifiez la ligne `from gpiozero import ...` pour remplacer `LED` par `TrafficLights`:

```python
Essayez de changer les feux à `blink`:

    ```python
while True:
    feux.blink()
    bouton.wait_for_press()
    feux.off()
    bouton.wait_for_press()
```

\--- /task \---