## GPIO-Komponenten

1. Öffne Python 3 aus dem Hauptmenü und öffne eine neue Datei.

2. Geben Sie den folgenden Code ein:
    
    ```python
von gpiozero importieren LED, Taste LED = LED (22) Taste = Taste (25) während True: wenn button.is_pressed: led.on () sonst: led.off ()
```

3. Führen Sie Ihren Code mit `F5`. Wenn Sie jetzt die Taste drücken, leuchtet die grüne LED auf.

4. Versuchen Sie, drei LEDs zu erstellen:
    
    ```python
von gpiozero import LED, Taste rot = LED (24) gelb = LED (23) grün = LED (22) Taste = Taste (25)
```

5. Lassen Sie sie beim Drücken der Taste einschalten:
    
    ```python
while True: if button.is_pressed: green.on () amber.on () red.on () else: green.off () amber.off () red.off ()
```

6. Führen Sie den Code aus und drücken Sie die Taste.