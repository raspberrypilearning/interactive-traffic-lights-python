## چراغ راهنمایی

شما می توانید از ساخته شده است در `TrafficLights` رابط کاربری به جای سه LED.

1. اصلاح `از gpiozero import ...` خط برای جایگزینی `LED` با `TrafficLights`:
    
    ```python
از gpiozero import TrafficLights، Button از دکمه زمان ورود واردات = دکمه (25) lights = TrafficLights (24، 23، 22) در حالی که True: button.wait_for_press () lights.on () button.wait_for_release () lights.off ()
```

2. سعی کنید نور را عوض کنید `blink`:
    
    ```python
در حالی که True: lights.blink () button.wait_for_press () lights.off () button.wait_for_release ()
```