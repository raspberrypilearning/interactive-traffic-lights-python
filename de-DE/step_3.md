## GPIO-Komponenten

1. Öffne Python 3 aus dem Hauptmenü und öffne eine neue Datei.

2. Gib den folgenden Code ein:
    
    ```python
from gpiozero import LED, Button

led = LED(22)
taster = Button(25)

while True:
    if taster.is_pressed:
        led.on()
    else:
        led.off()
```

3. Führe deinen Code mit `F5` aus. Wenn du jetzt die Taste drückst, leuchtet die grüne LED auf.

4. Versuche drei LEDs zu erstellen:
    
    ```python
from gpiozero import LED, Button

rot = LED(24)
gelb = LED(23)
gruen = LED(22)

taster = Button(25)
```

5. Lasse sie beim Drücken der Taste einschalten:
    
    ```python
while True:
    if taster.is_pressed:
        gruen.on()
        gelb.on()
        rot.on()
    else:
        gruen.off()
        gelb.off()
        rot.off()
```

6. Führe den Code aus und drücke die Taste.