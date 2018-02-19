## Componenti GPIO

1. Apri Python 3 dal menu principale e apri un nuovo file.

2. Inserisci il seguente codice:
    
    ```python
da gpiozero import LED, Button led = LED (22) button = Button (25) mentre True: if button.is_pressed: led.on () else: led.off ()
```

3. Esegui il tuo codice con `F5`. Ora quando si preme il pulsante, il LED verde si accende.

4. Prova a creare tre LED:
    
    ```python
da gpiozero import LED, pulsante rosso = LED (24) ambra = LED (23) verde = LED (22) pulsante = Pulsante (25)
```

5. Fai in modo che si accendano quando viene premuto il pulsante:
    
    ```python
while True: if button.is_pressed: green.on () amber.on () red.on () else: green.off () amber.off () red.off ()
```

6. Esegui il codice e premi il pulsante.