## GPIO-componenten

1. Open Python 3 in het hoofdmenu en open een nieuw bestand.

2. Voer de volgende code in:
    
    ```python
from gpiozero import LED, Button

led = LED(22)
button = Button(25)

while True:
    if button.is_pressed:
        led.on()
    else:
        led.off()
```

3. Voer je code uit met `F5`. Wanneer je nu op de knop drukt, gaat de groene LED branden.

4. Probeer drie LED's aan te sluiten:
    
    ```python
van gpiozero importeren LED, Knop rood = LED (24) oranje = LED (23) groen = LED (22) knop = Knop (25)
```

5. Laat ze komen als de knop wordt ingedrukt:
    
    ```python
while True: if button.is_pressed: green.on () amber.on () red.on () else: green.off () amber.off () red.off ()
```

6. Voer de code uit en druk op de knop.