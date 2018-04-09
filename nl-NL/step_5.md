## Volgorde verkeerslichten

Naast het besturen van alle LED's tegelijkertijd, kan je ze ook elk afzonderlijk bedienen. Met LEDs, een drukknop en een zoemer kan je jouw eigen verkeerslicht maken, compleet met oversteekplaats voor voetgangers !

1. Pas je lus aan om de LED's ​​automatisch in volgorde te laten branden:
    
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

2. Voeg een `wait_for_press ()` toe zodat het indrukken van de knop de reeks in gang zet:
    
    ```python
while True:
    button.wait_for_press()
    lights.groen.on()
    sleep(1)
    lights.oranje.on()
    sleep(1)
    lights.rood.on()
    sleep(1)
    lights.off()
```

Probeer je eigen reeks te maken.

3. Probeer nu de volledige reeks voor een verkeerslicht te maken:
    
    - Groen aan, rood uit
    - Oranje aan, groen uit
    - Rood aan, oranje uit
    - 
    - 
    
    Zorg ervoor dat de juiste lichten op het juiste moment worden in- en uitgeschakeld en zorg ervoor dat je steeds de juiste `sleep` periode gebruikt om de volgorde perfect te timen.

4. Probeer de knop voor een zebrapad toe te voegen. De knop moet de lichten (niet onmiddellijk) op rood zetten en de voetgangers de tijd geven om over te steken voordat de lichten weer groen worden totdat de knop opnieuw wordt ingedrukt.

5. Laat nu ten behoeve van visueel gehandicapte voetgangers een zoemer snel piepen om aan te geven dat het veilig is om over te steken.