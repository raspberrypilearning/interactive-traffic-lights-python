## Verkehrsampel

Du kannst die eingebaute `TrafficLights`-Schnittstelle statt drei LEDs verwenden.

1. Ändere die `from gpiozero import...`-Anweisung und ersetze `LED` mit `TrafficLights`:
    
    ```python
from gpiozero import TrafficLights, Button
from time import sleep

taster = Button(25)
lampen = TrafficLights(24, 23, 22)

while True:
    taster.wait_for_press()
    lampen.on()
    taster.wait_for_release()
    lampen.off()
```

2. Versuche den Befehl für die Lampen auf `blink` zu ändern:
    
    ```python
while True:
    lampen.blink()
    taster.wait_for_press()
    lampen.off()
    taster.wait_for_release()
```