## Verkehrsampel-Sequenz

Du kannst nicht nur die gesamte Lampengruppe steuern, sondern auch jede LED einzeln. Mit Ampel-LEDs, einem Taster und einem Summer kannst du deine eigene Ampel-Sequenz mit Fußgängerübergang erstellen!

1. Ändere deine Schleife, um folgenden automatisierten Ablauf der LEDs zu erzeugen:
    
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