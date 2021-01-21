## Последователност на светофарите

As well as controlling the whole set of lights together, you can also control each LED individually. With traffic light LEDs, a button, and a buzzer, you can create your own traffic lights sequence, complete with pedestrian crossing!

\--- task \---

Modify your loop to perform an automated sequence of LEDs being lit:

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

\--- /task \---

\--- task \---

Add a `wait_for_press()` so that pressing the button initiates the sequence:

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

\--- /task \---

\--- task \---

Now try creating the full traffic lights sequence:

- Зелено на
- Амбър на
- Червено включено
- Червено и кехлибарено
- Зелено на

Be sure to turn the correct lights on and off at the right time, and make sure you use `sleep` to time the sequence perfectly.

\--- /task \---

\--- task \---

Try adding the button for a pedestrian crossing. The button should move the lights to red (not immediately), and give the pedestrians time to cross before moving the lights back to green until the button is pressed again.

\--- /task \---

\--- task \---

Now try adding a buzzer to beep quickly to indicate that it is safe to cross, for the benefit of visually impaired pedestrians:

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