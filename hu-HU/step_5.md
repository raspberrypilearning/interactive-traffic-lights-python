## A közlekedési lámpa ciklusa

Az összes lámpa együttes vezérlésén kívül egyenként vezérelheted az egyes LED-eket is. A közlekedési lámpák LED-jei, a gombok és a berregő segítségével létrehozhatod a saját közlekedésilámpa-ciklusodat, beleértve a gyalogos átkelőt is!

\--- task \---

Módosítsd a ciklusodat, hogy automatikusan váltogassa az égő LED-eket:

```python
while True:
    lampak.green.on()
    sleep(1)
    lampak.amber.on()
    sleep(1)
    lampak.red.on()
    sleep(1)
    lampak.off()
```

\--- /task \---

\--- task \---

Adj hozzá egy `wait_for_press()` hívást, hogy a gomb megnyomására induljon a folyamat:

```python
while True:
    gomb.wait_for_press()
    lampak.green.on()
    sleep(1)
    lampak.amber.on()
    sleep(1)
    lampak.red.on()
    sleep(1)
    lampak.off()
```

Próbálj ki néhány saját ciklust.

\--- /task \---

\--- task \---

Most próbáld meg létrehozni a teljes lámpaciklust:

- Zöld bekapcsol
- Sárga bekapcsol
- Piros bekapcsol
- Piros és sárga bekapcsol
- Zöld bekapcsol

Győződj meg róla, hogy a helyes lámpákat kapcsolod be és ki a megfelelő időpontokban, és a `sleep` hívással időzítsd pontosra a ciklust.

\--- /task \---

\--- task \---

Próbálj meg hozzáadni egy gombot a gyalogos átkelőhöz. A gomb állítsa a lámpát pirosra (nem azonnal), és adjon időt a gyalogosoknak, hogy átkeljenek, mielőtt a lámpa visszavált zöldre a gomb következő megnyomásáig.

\--- /task \---

\--- task \---

Most próbálj meg hozzáadni egy berregőt, amely gyors hangjelzésekkel jelzi, hogy biztonságosan át lehet kelni, így segítve a látássérült gyalogosokat:

```python
berrego = Buzzer(15)

berrego.on()
berrego.off()
berrego.beep(0.1, 0.1)
```

\--- /task \---

A végső interaktív közlekedésilámpa-kódod a zöld lámpánál kezdődjön, aztán:

- Várja meg, hogy lenyomják a gombot
- Amikor lenyomták, váltson piros/sárgára, majd zöldre
- Adjon hangjelzéseket, amíg át lehet kelni
- Váltson sárgára, majd pirosra
- Ismételje meg