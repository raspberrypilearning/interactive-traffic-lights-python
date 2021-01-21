## यातायात बत्तिया

आप तीन अलग-अलग एलईडी के बजाय इन-बिल्ड ` ट्रैफिक लाइट </ 0> श्रेणी का उपयोग कर सकते हैं।</p>

<p>--- task ---</p>

<p>`from gpiozero import...` लाइन मे एलईडी को ट्रैफिक लाइट से बदल दो:</p>

<pre><code class="python">from gpiozero import TrafficLights, Button
from time import sleep

button = Button(21)
lights = TrafficLights(25, 28, 27)

while True:
    button.wait_for_press()
    lights.on()
    button.wait_for_release()
    lights.off()
`</pre> 

\--- /task \---

\--- task \---

लाइट को बदलने की कोशिश करें ` blink </ 0> से:</p>

<pre><code class="python">while True:
    lights.blink()
    button.wait_for_press()
    lights.off()
    button.wait_for_release()
`</pre> 

\--- /task \---