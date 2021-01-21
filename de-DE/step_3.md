## GPIO-Komponenten

led = LED(22) taster = Button(25)

while True: if taster.is_pressed: led.on() else: led.off()

\--- /task \---

\--- task \---

Gib den folgenden Code ein:

```python
```python
from gpiozero import LED, Button
```

\--- /task \---

\--- task \---

Führe deinen Code mit `F5` aus. Wenn du jetzt die Taste drückst, leuchtet die grüne LED auf.

\--- /task \---

\--- task \---

Try creating three LEDs:

```python
Versuche drei LEDs zu erstellen:

    ```python
from gpiozero import LED, Button

rot = LED(24)
gelb = LED(23)
gruen = LED(22)

taster = Button(25)
```

\--- /task \---

\--- task \---

Get them to come on when the button is pressed:

```python
while True:
if taster.is_pressed:
    gruen.on()
    gelb.on()
    rot.on()
else:
    gruen.off()
    gelb.off()
    rot.off()
```

\--- /task \---

\--- task \---

Führe den Code aus und drücke die Taste.

\--- /task \---