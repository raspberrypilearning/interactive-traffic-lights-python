## Verkeerslichten

U kunt de ingebouwde `TrafficLights` gebruiken interface in plaats van drie LED's.

1. Wijzig de `from gpiozero import ...` te vervangen regel `LED` met `TrafficLights`:
    
    ```python
van gpiozero importeren TrafficLights, Button from time import sleepknop = Button (25) lights = TrafficLights (24, 23, 22) while True: button.wait_for_press () lights.on () button.wait_for_release () lights.off ()
```

2. Probeer de verlichting te veranderen naar `knip`:
    
    ```python
while True: lights.blink () button.wait_for_press () lights.off () button.wait_for_release ()
```