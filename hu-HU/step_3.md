## Vezéreld a LED-eket és a gombot

\--- task \---

Indítsd el a **Mu**-t a főmenüből.

\--- /task \---

\--- task \---

Írd be az alábbi kódot:

```python
from gpiozero import LED, Button

piros = LED(25)
gomb = Button(21)

while True:
    if gomb.is_pressed:
        piros.on()
    else:
        piros.off()
```

\--- /task \---

\--- task \---

Futtasd a kódodat `F5`-tel. Ha most megnyomod a gombot, a piros LED bekapcsol.

\--- /task \---

\--- task \---

Próbálj meg létrehozni három LED-et:

```python
from gpiozero import LED, Button

piros = LED(25)
sarga = LED(28)
zold = LED(27)

button = Button(21)
```

\--- /task \---

\--- task \---

Érd el, hogy mindhárom bekapcsoljon, ha megnyomod a gombot:

```python
while True:
    if button.is_pressed:
        zold.on()
        sarga.on()
        piros.on()
    else:
        zold.off()
        sarga.off()
        piros.off()
```

\--- /task \---

\--- task \---

Futtasd a kódot és nyomd meg a gombot.

\--- /task \---