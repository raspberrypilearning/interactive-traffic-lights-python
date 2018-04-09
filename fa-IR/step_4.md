## چراغ راهنمایی

شما می توانید از رابط داخلی `TrafficLights`به جای سه LED استفاده کنید.

1. خط `from gpiozero import...` را با جایگزینی `TrafficLights` به جای `LED` اصلاح کنید:
    
    ```python
from gpiozero import TrafficLights, Button
from time import sleep

button = Button(25)
lights = TrafficLights(24, 23, 22)

while True:
    button.wait_for_press()
    lights.on()
    button.wait_for_release()
    lights.off()
```

2. سعی کنید روشن بودن را به `چشمک زدن` تغییر دهید:
    
    ```python
while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
```