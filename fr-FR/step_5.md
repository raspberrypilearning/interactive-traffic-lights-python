## Séquence de feux de circulation

En plus de contrôler l'ensemble des lumières ensemble, vous pouvez également contrôler chaque LED individuellement. Avec des voyants lumineux, un bouton et un buzzer, vous pouvez créer votre propre séquence de feux de circulation, avec un passage pour piétons!

1. Modifiez votre boucle pour exécuter une séquence automatisée de LED allumées:
    
    ```python
alors que True: lights.green.on () sleep (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

2. Ajouter un `wait_for_press ()` de sorte que le fait d'appuyer sur le bouton initie la séquence:
    
    ```python
alors que True: button.wait_for_press () lights.green.on () sleep (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

Essayez d'autres séquences de votre choix.

3. Maintenant, essayez de créer la séquence complète des feux de circulation:
    
    - Vert sur
    - Ambre sur
    - Rouge sur
    - Rouge et ambre sur
    - Vert sur
    
    Assurez-vous d'allumer et d'éteindre les bonnes lumières au bon moment, et assurez-vous d'utiliser `sleep` pour chronométrer la séquence parfaitement.

4. Essayez d'ajouter le bouton pour un passage pour piétons. Le bouton devrait faire passer les lumières au rouge (pas immédiatement), et donner aux piétons le temps de traverser avant de remettre les lumières au vert jusqu'à ce que le bouton soit pressé à nouveau.

5. Maintenant, essayez d'ajouter un signal sonore pour indiquer rapidement qu'il est sécuritaire de traverser, pour le bénéfice des piétons malvoyants.