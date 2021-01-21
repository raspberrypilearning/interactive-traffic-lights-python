## GPIOコンポーネント

\--- task \---

メインメニューから**Mu**を開きます。

\--- /task \---

\--- task \---

以下のコードを入力します。

```python
```python
gpiozeroインポートLEDから、ボタンled = LED（22）ボタン=ボタン（25）Trueの場合：button.is_pressed：led.on（）else：led.off（）
```

\--- /task \---

\--- task \---

Run your code with `F5`. Now when you press the button, the green LED will come on.

\--- /task \---

\--- task \---

Try creating three LEDs:

```python
from gpiozero import LED, Button

red = LED(25)
amber = LED(28)
green = LED(27)

button = Button(21)
```

\--- /task \---

\--- task \---

ボタンが押されたときにそれらが来るようにする：

```python
while：button.is_pressed：green.on（）amber.on（）red.on（）else：green.off（）amber.off（）red.off（）
```

\--- /task \---

\--- task \---

コードを実行し、ボタンを押します。

\--- /task \---