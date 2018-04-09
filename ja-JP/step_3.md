## GPIOコンポーネント

1. メインメニューからPython 3を開き、新しいファイルを開きます。

2. 以下のコードを入力します。
    
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

3. `F5`でコードを実行してください。 ボタンを押すと、緑色のLEDが点灯します。

4. 3つのLEDを作成してみてください。
    
    ```python
from gpiozero import LED, Button

red = LED(24)
amber = LED(23)
green = LED(22)

button = Button(25)
```

5. ボタンが押されたときにそれらが反応ようにします：
    
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

6. コードを実行し、ボタンを押します。