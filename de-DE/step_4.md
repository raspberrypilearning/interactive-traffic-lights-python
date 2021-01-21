## Verkehrsampel

Du kannst die eingebaute `TrafficLights`-Schnittstelle statt drei LEDs verwenden.

taster = Button(25) lampen = TrafficLights(24, 23, 22)

while True: taster.wait_for_press() lampen.on() taster.wait_for_release() lampen.off()

```python
```python
from gpiozero import TrafficLights, Button
from time import sleep
```

\--- /task \---

\--- task \---

Ändere die `from gpiozero import...`-Anweisung und ersetze `LED` mit `TrafficLights`:

```python
Versuche den Befehl für die Lampen auf `blink` zu ändern:

    ```python
while True:
    lampen.blink()
    taster.wait_for_press()
    lampen.off()
    taster.wait_for_release()
```

\--- /task \---