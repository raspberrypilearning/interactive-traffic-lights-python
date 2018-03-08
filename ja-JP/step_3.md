## GPIOコンポーネント

1. メインメニューからPython 3を開き、新しいファイルを開きます。

2. 次のコードを入力します。
    
    ```python
gpiozeroインポートLEDから、ボタンled = LED（22）ボタン=ボタン（25）Trueの場合：button.is_pressed：led.on（）else：led.off（）
```

3. `F5`でコードを実行してください。 ボタンを押すと、緑のLEDが点灯します。

4. 3つのLEDを作成してみてください。
    
    ```python
gpiozeroインポートLEDからボタン赤= LED（24）黄色= LED（23）緑= LED（22）ボタン=ボタン（25）
```

5. ボタンが押されたときにそれらが来るようにする：
    
    ```python
while：button.is_pressed：green.on（）amber.on（）red.on（）else：green.off（）amber.off（）red.off（）
```

6. コードを実行し、ボタンを押します。