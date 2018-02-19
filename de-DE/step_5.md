## Ampel Sequenz

Sie können nicht nur die gesamte Beleuchtungsgruppe steuern, sondern auch jede LED einzeln steuern. Mit Ampel-LEDs, einem Knopf und einem Summer können Sie Ihre eigene Ampel-Sequenz mit Fußgängerüberweg erstellen!

1. Ändern Sie Ihre Schleife, um eine automatisierte Sequenz von LEDs zu erzeugen, die leuchten:
    
    ```python
while True: lights.green.on () sleep (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

2. Fügen Sie ein `wait_for_press ()` hinzu so dass das Drücken der Taste die Sequenz initiiert:
    
    ```python
while True: button.wait_for_press () lights.green.on () sleep (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

Probieren Sie einige weitere Sequenzen aus.

3. Versuchen Sie nun, die vollständige Ampelsequenz zu erstellen:
    
    - Grün an
    - Bernstein an
    - Rot an
    - Rot und Bernstein an
    - Grün an
    
    Stellen Sie sicher, dass Sie die richtigen Lichter zur richtigen Zeit ein- und ausschalten, und stellen Sie sicher, dass Sie `sleep` verwenden um die Sequenz perfekt zu synchronisieren.

4. Fügen Sie den Knopf für einen Fußgängerüberweg hinzu. Die Taste sollte die Lichter auf rot (nicht sofort) bewegen und den Fußgängern Zeit zum Überqueren geben, bevor die Lichter wieder grün werden, bis die Taste erneut gedrückt wird.

5. Versuchen Sie jetzt, einen Summer hinzuzufügen, um schnell zu piepen, um anzuzeigen, dass es gefahrlos überquert werden kann, um sehbehinderten Fußgängern zu helfen.