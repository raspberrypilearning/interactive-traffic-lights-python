## GPIO-componenten

\--- task \---

Open **Mu** from the main menu.

\---/task\---

\--- task \---

Voer de volgende code in:

```python
from gpiozero import LED, Button

red = LED(25)
button = Button(21)

while True:
    if button.is_pressed:
        red.on()
    else:
        red.off()
```

\--- /task \---

\--- task \---

Voer je code uit met `F5`. Wanneer je nu op de knop drukt, gaat de groene LED branden.

\--- /task \---

\--- task \---

Probeer drie LED's aan te sluiten:

```python
from gpiozero import LED, Button

rood = LED(25)
oranje = LED(28)
groen = LED(27)

button = Button(21)
```

-- /task \---

\--- task \----

Laat ze oplichten als de knop wordt ingedrukt:

```python
while True:
    if button.is_pressed:
        groen.on()
        oranje.on()
        rood.on()
    else:
        groen.off()
        oranje.off()
        rood.off()
```

\--- /task \---

\--- taak \---

Voer de code uit en druk op de knop.

\--- /task \---