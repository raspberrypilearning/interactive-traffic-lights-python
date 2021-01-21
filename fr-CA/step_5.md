## Séquence de feux de circulation

En plus de contrôler les feux tous ensemble, vous pouvez aussi contrôler les DELs individuellement. Avec des DELs, un bouton et un avertisseur sonore, vous pouvez créer votre propre séquence de feux de circulation complète, avec une traverse de piétons!

Essayez d'autres séquences de votre choix.

Modifiez votre boucle pour exécuter une séquence automatisée d'allumage de DELs:

```python
```python
while True:
feux.green.on()
sleep(1)
feux.amber.on()
sleep(1)
feux.red.on()
sleep(1)
feux.off()
```

...

\--- task \---

Add a `wait_for_press()` so that pressing the button initiates the sequence:

```python
Ajouter un `wait_for_press()` de sorte que le fait d'appuyer sur le bouton initie la séquence:

    ```python
while True:
    bouton.wait_for_press()
    feux.green.on()
    sleep(1)
    feux.amber.on()
    sleep(1)
    feux.red.on()
    sleep(1)
    feux.off()
```

Try some more sequences of your own.

\--- /task \---

\--- task \---

Maintenant, essayez de créer la séquence complète des feux de circulation:

- Rouge on
- Jaune on
- Vert on
- Red and amber on
- Vert on

Assurez-vous d'allumer et d'éteindre les bons feux au bon moment et assurez-vous d'utiliser `sleep` pour contrôler la durée de chaque étape la séquence.

\--- /task \---

\--- task \---

Essayez d'ajouter le bouton pour un passage pour piétons. Le bouton devrait faire passer les feux au rouge (pas immédiatement), et donner aux piétons le temps de traverser avant de remettre les feux au vert, jusqu'à ce que le bouton soit pressé à nouveau.

\--- /task \---

\--- task \---

Maintenant essayez d'ajouter un bip sonore rapide pour indiquer aux personnes malvoyantes qu'il est sécuritaire de traverser.

```python
buzzer = Buzzer(15)

buzzer.on()
buzzer.off()
buzzer.beep(0.1, 0.1)
```

\--- /task \---

Your final interactive traffic lights code should start on a green light and then:

- Wait for the button to be pressed
- When pressed, change to red/amber, then green
- Beep for a while to say it's time to cross
- Go to amber and then green
- Repeat