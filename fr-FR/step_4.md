## Feux de circulation

Vous pouvez utiliser la fonction intégrée `TrafficLights` interface au lieu de trois LED.

1. Modifier le `depuis gpiozero import ...` ligne à remplacer `LED` avec `TrafficLights`:
    
    ```python
à partir de gpiozero import TrafficLights, bouton de temps import bouton de veille = Button (25) lights = TrafficLights (24, 23, 22) alors que True: button.wait_for_press () lights.on () button.wait_for_release () lights.off ()
```

2. Essayez de changer les lumières à `blink`:
    
    ```python
alors que True: lights.blink () button.wait_for_press () lights.off () button.wait_for_release ()
```