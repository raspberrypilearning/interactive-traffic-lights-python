## GPIO components

1. Open Python 3 from the main menu, and open a new file.

1. Enter the following code:

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

1. Run your code with `F5`. Now when you press the button, the green LED will come on.

1. Try creating three LEDs:

    ```python
    from gpiozero import LED, Button

    red = LED(24)
    amber = LED(23)
    green = LED(22)

    button = Button(25)
    ```

1. Get them to come on when the button is pressed:

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

1. Run the code and press the button.
