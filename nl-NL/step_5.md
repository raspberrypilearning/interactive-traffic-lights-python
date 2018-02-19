## Verkeerslichten volgorde

Behalve dat je alle LED's tegelijkertijd bestuurt, kunt je ook elke led afzonderlijk bedienen. Met traffic light LEDs, een knop en een zoemer kunt je jouw eigen verkeerslichtreeks creëren, compleet met voetgangersoversteekplaats!

1. Pas je lus aan om een de reeks LED's ​​geautomatiseerde te laten branden:
    
    ```python
while True:
    lights.groen.on()
    sleep(1)
    lights.oranje.on()
    sleep(1)
    lights.rood.on()
    sleep(1)
    lights.off()
```

2. Voeg een `wait_for_press ()` toe zodat het indrukken van de knop de reeks initieert:
    
    ```python
while True: button.wait_for_press () lights.green.on () sleep (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

Probeer nog wat meer eigen reeksen.

3. Probeer nu de volledige reeks verkeerslichten te maken:
    
    - Groen aan
    - Amber aan
    - Rood aan
    - Rood en oranje op
    - Groen aan
    
    Zorg ervoor dat de juiste lichten op het juiste moment worden in- en uitgeschakeld en zorg ervoor dat u `slaap` om de volgorde perfect te timen.

4. Probeer de knop toe te voegen voor een zebrapad. De knop moet de lichten naar rood (niet onmiddellijk) verplaatsen en de voetgangers de tijd geven om over te steken voordat de lichten weer groen worden totdat de knop opnieuw wordt ingedrukt.

5. Probeer nu een zoemer toe te voegen om snel te piepen om aan te geven dat het veilig is om over te steken, ten behoeve van visueel gehandicapte voetgangers.