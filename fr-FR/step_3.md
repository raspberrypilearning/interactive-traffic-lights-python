## Contrôler les LED et le bouton

\--- task \---

Ouvre **Mu** depuis le menu principal.

\--- /task \---

\--- task \---

Entre la commande suivante :

```python
from gpiozero import LED, Button

rouge = LED(25)
bouton = Button(21)

while True:
    if bouton.is_pressed:
        rouge.on()
    else:
        rouge.off()
```

\--- /task \---

\--- task \---

Exécute le code avec `F5`. Maintenant, quand tu appuies sur le bouton, la LED rouge va s'allumer.

\--- /task \---

\--- task \---

Essaie de créer trois LEDs :

```python
from gpiozero import LED, Button

rouge = LED(25)
orange = LED(28)
vert = LED(27)

bouton = Button(21)
```

\--- /task \---

\--- task \---

Fais en sorte qu'ils s'allument s'allumer lorsque le bouton est pressé :

```python
while True:
    if bouton.is_pressed:
        vert.on()
        orange.on()
        rouge.on()
    else:
        vert.off()
        orange.off()
        rouge.off()
```

\--- /task \---

\--- task \---

Exécute le code et appuie sur le bouton.

\--- /task \---