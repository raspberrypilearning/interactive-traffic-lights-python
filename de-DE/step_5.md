## Verkehrsampel Sequenz

Du kannst nicht nur die gesamte Lampengruppe steuern, sondern auch jede LED einzeln. Mit Ampel-LEDs, einem Taster und einem Summer kannst du deinen eigenen Ampel-Ablauf mit Fußgängerübergang erstellen!

Red, amber und green sind Parameter des TrafficLight-APIs und stehen für die Farben rot, gelb und grün.

Probiere einige weitere Abläufe aus.

```python
```python
while True:
lampen.green.on()
sleep(1)
lampen.amber.on()
sleep(1)
lampen.red.on()
sleep(1)
lampen.off()
```

\--- /task \---

\--- task \---

Add a `wait_for_press()` so that pressing the button initiates the sequence:

```python
Füge ein `wait_for_press ()` hinzu so dass das Drücken der Taste die Sequenz startet:

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

Try some more sequences of your own.

\--- /task \---

\--- task \---

Versuche nun, den vollständigen Ampel-Ablauf zu erstellen:

- Grün an
- Gelb an
- Rot an
- Rot und Gelb an
- Grün an

Stelle sicher, dass die richtigen Lichter zur richtigen Zeit ein- und ausschalten, und stelle sicher, dass du `sleep` verwendest um den richtigen Zeitablauf zu haben.

\--- /task \---

\--- task \---

Füge den Knopf für einen Fußgängerübergang hinzu. Die Taste sollte die Ampel auf rot (nicht sofort) stellen und den Fußgängern Zeit zum Überqueren geben, bevor die Ampel wieder grün wird.

\--- /task \---

\--- task \---

Versuche jetzt, einen Summer hinzuzufügen, der schnell piept, um sehbehinderten Fußgängern anzuzeigen, dass sie gefahrlos überqueren können.

```python
buzzer = Buzzer(15)

buzzer.on()
buzzer.off()
buzzer.beep(0.1, 0.1)
```

\--- /task \---

Your final interactive traffic lights code should start on a green light and then:

- Wait for the button to be pressed
- When pressed, change to red/amber, then green
- Beep for a while to say it's time to cross
- Go to amber and then green
- Repeat