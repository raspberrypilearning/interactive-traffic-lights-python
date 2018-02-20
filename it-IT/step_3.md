## Componenti GPIO

1. Lancia Python 3 dal menu principale e apri un nuovo file.

2. Inserisci il seguente codice:
    
    ```python
from gpiozero import LED, Button

led = LED(22)
pulsante = Button(25)

while True:
    if pulsante.is_pressed:
        led.on()
    else:
        led.off()
```

3. Esegui il programma con `F5`. Quando premerai il pulsante, il LED verde si accenderà.

4. Prova a creare tre LED:
    
    ```python
from gpiozero import LED, Button

rosso = LED(24)
ambra = LED(23)
verde = LED(22)

pulsante = Button(25)
```

5. Fai in modo che si accendano quando viene premuto il pulsante:
    
    ```python
while True:
    if pulsante.is_pressed:
        verde.on()
        ambra.on()
        rosso.on()
    else:
        verde.off()
        ambra.off()
        rosso.off()
```

6. Esegui il programma e premi il pulsante.