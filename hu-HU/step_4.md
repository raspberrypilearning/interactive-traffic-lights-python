## Közlekedési lámpák

Használhatja a beépített `TrafficLights` -t három LED helyett.

1. A `a gpiozero import ...` módosítása | vonal helyett `LED` `TrafficLights`:
    
    ```python
a gpiozero importálással TrafficLights, gomb az importálás pillanatától kezdve = gomb (25) világít = TrafficLights (24, 23, 22), miközben True: gomb.wait_for_press () lights.on () gomb.wait_for_release () lights.off ()
```

2. Próbálja megváltoztatni a fényeket a `villog`:
    
    ```python
míg a True: lights.blink () gomb.wait_for_press () lights.off () gomb.wait_for_release ()
```