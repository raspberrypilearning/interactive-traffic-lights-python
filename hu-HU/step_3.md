## GPIO komponensek

1. Nyissa meg a Python 3-at a főmenüből, és nyisson meg egy új fájlt.

2. Adja meg a következő kódot:
    
    ```python
a gpiozero import LED, a gomb led = LED (22) gomb = gomb (25), míg a True: ha a gomb megnyomva: led.on () else: led.off ()
```

3. Futtassa a kódot a `F5`paranccsal. Most, amikor megnyomja a gombot, megjelenik a zöld LED.

4. Próbáljon három LED-et létrehozni:
    
    ```python
gpiozero import LED, gomb piros = LED (24) sárga = LED (23) zöld = LED (22) gomb = gomb (25)
```

5. Vigye be őket a gomb megnyomásakor.
    
    ```python
míg a True: ha gomb megnyomva: green.on () amber.on () red.on () else: green.off () amber.off () red.off ()
```

6. Futtassa a kódot, és nyomja meg a gombot.