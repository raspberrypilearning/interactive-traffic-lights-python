## Ampeln

Sie können das eingebaute `TrafficLights` verwenden Schnittstelle statt drei LEDs.

1. Ändern Sie die `von gpiozero import ...` zu ersetzende Zeile `LED` mit `TrafficLights`:
    
    ```python
von gpiozero Importiere TrafficLights, Button aus der Zeit import sleep button = Button (25) lights = TrafficLights (24, 23, 22) während True: button.wait_for_press () lights.on () button.wait_for_release () lights.off ()
```

2. Versuchen Sie, die Lichter zu ändern: `blink`:
    
    ```python
wahr: lights.blink () button.wait_for_press () lights.off () button.wait_for_release ()
```