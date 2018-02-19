## Traffic lights sequence

As well as controlling the whole set of lights together, you can also control each LED individually. With traffic light LEDs, a button, and a buzzer, you can create your own traffic lights sequence, complete with pedestrian crossing!

1. Modify your loop to perform an automated sequence of LEDs being lit:
    
    ```python
while True:
    lights.green.on()
    sleep(1)
    lights.amber.on()
    sleep(1)
    lights.red.on()
    sleep(1)
    lights.off()
```

2. Add a `wait_for_press()` so that pressing the button initiates the sequence:
    
    ```python
while True:
    button.wait_for_press()
    lights.green.on()
    sleep(1)
    lights.amber.on()
    sleep(1)
    lights.red.on()
    sleep(1)
    lights.off()
```

Try some more sequences of your own.

3. Now try creating the full traffic lights sequence:
    
    - Green on
    - Amber on
    - Red on
    - Red and amber on
    - Green on
    
    Be sure to turn the correct lights on and off at the right time, and make sure you use `sleep` to time the sequence perfectly.

4. Try adding the button for a pedestrian crossing. The button should move the lights to red (not immediately), and give the pedestrians time to cross before moving the lights back to green until the button is pressed again.

5. Now try adding a buzzer to beep quickly to indicate that it is safe to cross, for the benefit of visually impaired pedestrians.