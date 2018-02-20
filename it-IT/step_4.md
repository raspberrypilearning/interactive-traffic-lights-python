## Semafori

È possibile utilizzare l'interfaccia `TrafficLights` al posto dei tre LED.

1. Modifica la riga `from gpiozero import...` sostituiendo `LED` con `TrafficLights`:
    
    ```python
from gpiozero import TrafficLights, Button
from time import sleep

button = Button(25)
lights = TrafficLights(24, 23, 22)

while True:
    button.wait_for_press()
    lights.on()
    button.wait_for_release()
    lights.off()
```

2. Prova a modificare il comportamento delle luci con `blink`:
    
    ```python
while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
```