## Componenti GPIO

led = LED(22) button = Button(25)

while True: if button.is_pressed: led.on() else: led.off()

\--- /task \---

\--- task \---

Inserisci il seguente codice:

```python
```python
from gpiozero import LED, Button
```

\--- /task \---

\--- task \---

Esegui il programma con `F5`. Quando premerai il pulsante, il LED verde si accenderà.

\--- /task \---

\--- task \---

Try creating three LEDs:

```python
Prova a creare tre LED:

    ```python
from gpiozero import LED, Button

red = LED(24)
amber = LED(23)
green = LED(22)

button = Button(25)
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