## اجزای GPIO

1. پایتون 3 را از منوی اصلی باز کنید و فایل جدیدی باز کنید.

2. کد زیر را وارد کنید:
    
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

3. کد خود را با `F5` اجرا کنید. حالا وقتی دکمه را فشار می دهید، چراغ سبز روشن می شود.

4. ایجاد سه Led را امتحان کنید:
    
    ```python
from gpiozero import LED, Button

red = LED(24)
amber = LED(23)
green = LED(22)

button = Button(25)
```

5. کاری کنید که وقتی دکمه فشرده می‌شود، آن‌ها روشن شوند:
    
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

6. کد را اجرا کنید و دکمه را فشار دهید.