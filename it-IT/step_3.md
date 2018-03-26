## Componenti GPIO

1. Lancia Python 3 dal menu principale e apri un nuovo file.

2. Inserisci il seguente codice:
    
    ```python
from gpiozero import LED, Button

led = LED(22)
button = Button(25)

while True:
    if button.is_pressed:
        led.on()
    else:
        led.off()
```

3. Esegui il programma con `F5`. Quando premerai il pulsante, il LED verde si accenderà.

4. Prova a creare tre LED:
    
    ```python
from gpiozero import LED, Button

red = LED(24)
amber = LED(23)
green = LED(22)

button = Button(25)
```

5. Fai in modo che si accendano quando viene premuto il pulsante:
    
    ```python
while True:
    if button.is_pressed:
        green.on()
        amber.on()
        red.on()
    else:
        green.off()
        amber.off()
        red.off()
```

6. Esegui il programma e premi il pulsante.