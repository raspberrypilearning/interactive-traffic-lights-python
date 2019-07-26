## Séquence de feux de circulation

En plus de contrôler l'ensemble des lumières, tu peux également contrôler chaque LED individuellement. Avec des voyants lumineux, un bouton et un buzzer, tu peux créer ta propre séquence de feux de circulation, avec un passage pour piétons !

\--- task \---

Modifie ta boucle pour exécuter une séquence automatisée d'allumage des LEDs:

```python
while True:
    lumieres.vert.on()
    sleep(1)
    lumieres.orange.on()
    sleep(1)
    lumieres.rouge.on()
    sleep(1)
    lumieres.off()
```

\--- /task \---

\--- task \---

Ajoute un `wait_for_press()` de sorte que le fait d'appuyer sur le bouton lance la séquence:

```python
while True:
    bouton.wait_for_press()
    lumieres.vert.on()
    sleep(1)
    lumieres.orange.on()
    sleep(1)
    lumieres.rouge.on()
    sleep(1)
    lumieres.off()
```

Essaie plus de séquences de ton choix.

\--- /task \---

\--- task \---

Maintenant essaie de faire la séquence complète que l'on trouve au Royaume-Uni pour les feux de signalisations:

- Vert allumé
- Orange allumé
- Rouge allumé
- Rouge et orange allumé
- Vert allumé

Assure-toi d'allumer et d'éteindre la bonne lumière au bon moment, et vérifie que tu utilises `sleep` pour que la séquence soit parfaitement synchronisée.

\--- /task \---

\--- task \---

Essaie d'ajouter le bouton pour le passage piéton. Le bouton devra changer de couleur et passer au rouge (pas immédiatement), et laisser aux piétons le temps de traverser avant que le feux vert ne soit redonné jusqu'à ce que le bouton soit à nouveau actionné.

\--- /task \---

\--- task \---

Maintenant essaie d'implémenter un bref bip via le buzzer pour indiquer aux piétons malvoyants que l'on peut traverser sans danger :

```python
buzzer = Buzzer(15)

buzzer.on()
buzzer.off()
buzzer.beep(0.1, 0.1)
```

\--- /task \---

Ton code de feux de signalisation interactif doit commencer par un feu vert puis :

- Attendre que le bouton soit appuyé
- Quand il est appuyé, change le feu en orange puis rouge
- Fais biper pendant un moment pour signaler qu'il est temps de traverser
- Passer au rouge et orange puis au vert
- Répéter