## Composants GPIO

led = LED(22) bouton = Button(25)

while True: if bouton.is_pressed: led.on() else: led.off()

\---tâche\---

\---tâche\---

Entrez le code suivant:

```python
```python
from gpiozero import LED, Button
```

\---tâche\---

\---tâche\---

Exécutez votre code avec la touche `F5` . Maintenant, lorsque vous appuyez sur le bouton, la DEL verte s'allume.

\---tâche\---

\---tâche\---

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

\---tâche\---

\---tâche\---

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

\---tâche\---

\---tâche\---

Exécutez le code et appuyez sur le bouton.

\---tâche\---