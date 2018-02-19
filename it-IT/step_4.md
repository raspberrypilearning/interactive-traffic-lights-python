## Semafori

È possibile utilizzare il built-in `TrafficLights` interfaccia invece di tre LED.

1. Modificare il valore `da gpiozero import ...` riga da sostituire `LED` con `TrafficLights`:
    
    ```python
da gpiozero import TrafficLights, Pulsante da time sleep di importazione tasto = Button (25) lights = TrafficLights (24, 23, 22) mentre True: button.wait_for_press () lights.on () button.wait_for_release () lights.off ()
```

2. Prova a cambiare le luci su `lampeggiare`:
    
    ```python
while True: lights.blink () button.wait_for_press () lights.off () button.wait_for_release ()
```