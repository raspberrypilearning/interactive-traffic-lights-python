## 交通信号灯

組み込み`TrafficLights`を使用できます。 3つのLEDの代わりに使用できます。

1. `gpiozeroインポートからの修正|`交換する線`LED` `TrafficLights`：
    
    ```python
トラフィックライト、時刻からのボタンの読み込みボタン=ボタン（25）lights = TrafficLights（24,23,22）while：button.wait_for_press（）lights.on（）button.wait_for_release（）lights.off（）
```

2. ライトを`blink`に変更してみてください：
    
    ```python
true：lights.blink（）button.wait_for_press（）lights.off（）button.wait_for_release（）
```