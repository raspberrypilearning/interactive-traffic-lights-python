## एल ई डी और बटन को नियंत्रित करें

\--- task \---

मुख्य मेनू से **Mu** खोलें।

\--- /task \---

\--- task \---

निम्नलिखित कोड को दर्ज करें:

```python
from gpiozero import LED, Button

red = LED(25)
button = Button(21)

while True:
    if button.is_pressed:
        red.on()
    else:
        red.off()
```

\--- /task \---

\--- task \---

अपना कोड ` F5 </ 0> के साथ चलाएं। अब जब आप बटन दबाएंगे, तो हरे रंग की एलईडी आएगी।</p>

<p>--- /task ---</p>

<p>--- task ---</p>

<p>तीन एलईडी के साथ अब कोशिश करें:</p>

<pre><code class="python">from gpiozero import LED, Button

red = LED(25)
amber = LED(28)
green = LED(27)

button = Button(21)
`</pre> 

\--- /task \---

\--- task \---

बटन दबाए जाने पर उन एल ई डी को ऑन करे:

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

\--- /task \---

\--- task \---

कोड चलाएं और फिर बटन दबाएं।

\--- /task \---