## Composants GPIO

1. Lancez Python 3 à partir du menu principal et ouvrez un nouveau fichier.

2. Entrez le code suivant:
    
    ```python
from gpiozero import LED, Button

led = LED(22)
bouton = Button(25)

while True:
    if bouton.is_pressed:
        led.on()
    else:
        led.off()
```

3. Exécutez votre code avec la touche `F5` . Maintenant, lorsque vous appuyez sur le bouton, la DEL verte s'allume.

4. Essayez de créer trois DELs:
    
    ```python
from gpiozero import LED, Button

rouge = LED(24)
jaune = LED(23)
vert = LED(22)

bouton = Button(25)
```

5. Faites les allumer lorsque le bouton est pressé:
    
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

6. Exécutez le code et appuyez sur le bouton.