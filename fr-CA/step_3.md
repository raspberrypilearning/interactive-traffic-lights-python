## Composants GPIO

led = LED(22) bouton = Button(25)

while True: if bouton.is_pressed: led.on() else: led.off()

\--- /task \---

\--- task \---

Entrez le code suivant:

```python
```python
from gpiozero import LED, Button
```

\--- /task \---

\--- task \---

Exécutez votre code avec la touche `F5` . Maintenant, lorsque vous appuyez sur le bouton, la DEL verte s'allume.

\--- /task \---

\--- task \---

Try creating three LEDs:

```python
Essayez de créer trois DELs:

    ```python
from gpiozero import LED, Button

rouge = LED(24)
jaune = LED(23)
vert = LED(22)

bouton = Button(25)
```

\--- /task \---

\--- task \---

Faites les allumer lorsque le bouton est pressé:

```python
while True:
if bouton.is_pressed:
    vert.on()
    jaune.on()
    rouge.on()
else:
    green.off()
    jaune.off()
    rouge.off()
```

\--- /task \---

\--- task \---

Exécutez le code et appuyez sur le bouton.

\--- /task \---