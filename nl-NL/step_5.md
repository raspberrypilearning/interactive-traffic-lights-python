## Verkeerslichten volgorde

Naast het besturen van alle LED's tegelijkertijd, kan je ze ook elk afzonderlijk bedienen. Met LEDs, een drukknop en een zoemer kan je jouw eigen verkeerslicht maken, compleet met oversteekplaats voor voetgangers !

--- task ---

Pas je lus aan om de LED's ​​automatisch in volgorde te laten branden:

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

--- /task ---

--- task ---

Voeg een `wait_for_press ()` toe zodat het indrukken van de knop de reeks in gang zet:

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

--- /task ---

--- task ---

Probeer nu de volledige reeks voor een verkeerslicht te maken:

- Rood uit en groen aan
- Groen uit, oranje aan
- Oranje uit, rood aan
- 
- Rood uit en groen aan

Zorg ervoor dat de juiste lichten op het juiste moment worden in- en uitgeschakeld en zorg ervoor dat je steeds de juiste `sleep` periode gebruikt om de volgorde perfect te timen.

--- /task ---

--- task ---

Probeer de knop voor een zebrapad toe te voegen. De knop moet de lichten (niet onmiddellijk) op rood zetten en de voetgangers de tijd geven om over te steken voordat de lichten weer groen worden totdat de knop opnieuw wordt ingedrukt.

--- /task ---

--- task ---

Laat nu ten behoeve van visueel gehandicapte voetgangers een zoemer snel piepen om aan te geven dat het veilig is om over te steken:

```python
buzzer = Buzzer(15)

buzzer.on()
buzzer.off()
buzzer.beep(0.1, 0.1)
```

--- /task ---

Je laatste interactieve verkeerslichtcode moet beginnen met een groen licht en vervolgens:

- Wacht tot de knop wordt ingedrukt
- Wanneer ingedrukt, verander naar rood/oranje, dan groen
- Piep een tijdje om te zeggen dat het tijd is om over te steken
- Ga naar oranje en vervolgens groen
- Herhaal
***
Dit project werd vertaald door vrijwilligers:

Robert-Jan Kempenaar
Coen Warries
Sanneke van der Meer
Cor Groot
Jeroen Dekker

Dankzij vrijwilligers kunnen we mensen over de hele wereld de kans geven om in hun eigen taal te leren. Jij kunt ons helpen meer mensen te bereiken door vrijwillig te starten met vertalen - meer informatie op [rpf.io/translate](https://rpf.io/translate).
