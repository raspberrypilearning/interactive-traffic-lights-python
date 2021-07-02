## Controlla i LED ed il pulsante

\--- task \---

Apri **Mu** dal menu principale.

\--- /task \---

\--- task \---

Inserisci il seguente codice:

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

Esegui il programma premendo `F5`. Quando premerai il pulsante, il LED rosso si accenderà.

\--- /task \---

\--- task \---

Prova a creare tre LED:

```python
from gpiozero import LED, Button

red = LED(25)
amber = LED(28)
green = LED(27)

button = Button(21)
```

\--- /task \---

\--- task \---

Fai in modo che si accendano quando viene premuto il pulsante:

```python
while True:
    if button.is_pressed:
        green.on()
        amber.on()
        red.on()
    else:
        green.off()
        amber.off()
        red.off()
```

\--- /task \---

\--- task \---

Esegui il programma e premi il pulsante.

\--- /task \---