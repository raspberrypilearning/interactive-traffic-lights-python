## 信号機

組み込み`TrafficLights`を使用できます。 3つのLEDの代わりに使用できます。

\--- task \---

`gpiozeroインポートからの修正|`交換する線`LED` `TrafficLights`：

```python
```python
トラフィックライト、時刻からのボタンの読み込みボタン=ボタン（25）lights = TrafficLights（24,23,22）while：button.wait_for_press（）lights.on（）button.wait_for_release（）lights.off（）
```

\--- /task \---

\--- task \---

Try changing the lights to `blink`:

```python
ライトを`blink`に変更してみてください：

    ```python
true：lights.blink（）button.wait_for_press（）lights.off（）button.wait_for_release（）
```

\--- /task \---