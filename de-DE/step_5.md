## Verkehrsampel-Sequenz

Du kannst nicht nur die gesamte Lampengruppe steuern, sondern auch jede LED einzeln. Mit Ampel-LEDs, einem Taster und einem Summer kannst du deine eigene Ampel-Sequenz mit Fußgängerübergang erstellen!

1. Ändere deine Schleife, um folgenden automatisierten Ablauf der LEDs zu erzeugen:
    
    ```python
while True:
    lampen.green.on()
    sleep(1)
    lampen.amber.on()
    sleep(1)
    lampen.red.on()
    sleep(1)
    lampen.off()

Red, amber und green sind Parameter des TrafficLight-APIs und stehen für die Farben rot, gelb und grün.
```

2. Füge ein `wait_for_press ()` hinzu so dass das Drücken der Taste die Sequenz startet:
    
    ```python
while True:
    taster.wait_for_press()
    lampen.green.on()
    sleep(1)
    lampen.amber.on()
    sleep(1)
    lampen.red.on()
    sleep(1)
    lampen.off()
```

Probiere einige weitere Sequenzen aus.

3. Versuche nun, die vollständige Ampelsequenz zu erstellen:
    
    - Grün an
    - Gelb an
    - Rot an
    - Rot und Gelb an
    - Grün an
    
    Stelle sicher, dass die richtigen Lichter zur richtigen Zeit ein- und ausschalten, und stelle sicher, dass du `sleep` verwendest um den richtigen Zeitablauf zu haben.

4. Füge den Knopf für einen Fußgängerübergang hinzu. Die Taste sollte die Ampel auf rot (nicht sofort) stellen und den Fußgängern Zeit zum Überqueren geben, bevor die Ampel wieder grün wird. Die Ampel bleibt grün bis die Taste erneut gedrückt wird.

5. Versuche jetzt, einen Summer hinzuzufügen, der schnell piept, um sehbehinderten Fußgängern anzuzeigen, dass sie gefahrlos überqueren können.