## Séquence de feux de circulation

En plus de contrôler les feux tous ensemble, vous pouvez aussi contrôler les DELs individuellement. Avec des DELs, un bouton et un avertisseur sonore, vous pouvez créer votre propre séquence de feux de circulation complète, avec une traverse de piétons!

1. Modifiez votre boucle pour exécuter une séquence automatisée d'allumage de DELs:
    
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

2. Ajouter un `wait_for_press()` de sorte que le fait d'appuyer sur le bouton initie la séquence:
    
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

Essayez d'autres séquences de votre choix.

3. Maintenant, essayez de créer la séquence complète des feux de circulation:
    
    - Vert on
    - Jaune on
    - Rouge on
    - Vert on
    - ...
    
    Assurez-vous d'allumer et d'éteindre les bons feux au bon moment et assurez-vous d'utiliser `sleep` pour contrôler la durée de chaque étape la séquence.

4. Essayez d'ajouter le bouton pour un passage pour piétons. Le bouton devrait faire passer les feux au rouge (pas immédiatement), et donner aux piétons le temps de traverser avant de remettre les feux au vert, jusqu'à ce que le bouton soit pressé à nouveau.

5. Maintenant essayez d'ajouter un bip sonore rapide pour indiquer aux personnes malvoyantes qu'il est sécuritaire de traverser.