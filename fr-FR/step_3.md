## Composants GPIO

1. Ouvrez Python 3 à partir du menu principal et ouvrez un nouveau fichier.

2. Entrez le code suivant:
    
    ```python
à partir de LED d'importation gpiozero, bouton led = LED (22) bouton = bouton (25) alors que vrai: si button.is_pressed: led.on () else: led.off ()
```

3. Lancez votre code avec `F5`. Maintenant, lorsque vous appuyez sur le bouton, la LED verte s'allume.

4. Essayez de créer trois LED:
    
    ```python
à partir de la LED d'importation gpiozero, bouton rouge = LED (24) ambre = LED (23) vert = LED (22) touche = Bouton (25)
```

5. Amenez-les à venir quand le bouton est pressé:
    
    ```python
alors que True: si button.is_pressed: green.on () amber.on () red.on () sinon: green.off () amber.off () red.off ()
```

6. Exécutez le code et appuyez sur le bouton.