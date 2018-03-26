## A közlekedési lámpa sorrendje

Az összes lámpa együttes vezérlésével egyenként vezérelheti az egyes LED-eket is. A közlekedési lámpák LED-jei, a gombok és a hangjelző segítségével létrehozhat saját forgalmi jelzőlámpákat, valamint a gyalogos átkelést!

1. Módosítsa hurokját a LED-ek automatizált sorrendjének végrehajtására:
    
    ```python
míg a True: lights.green.on () alvás (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

2. Add hozzá `wait_for_press ()` így a gomb lenyomása kezdeményezi a sorrendet:
    
    ```python
míg az Igaz: button.wait_for_press () lights.green.on () sleep (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

Próbálj ki néhány saját szekvenciát.

3. Most próbáld ki a teljes közlekedési lámpa szekvenciát:
    
    - Zölden
    - Borostyán
    - Piros
    - Piros és sárga
    - Zölden
    
    Győződjön meg róla, hogy a helyes fényeket be- és kikapcsolja a megfelelő időben, és győződjön meg róla, hogy a `alvás` hogy a szekvencia tökéletesen megfeleljen.

4. Próbálja meg hozzáadni a gyalogos átkeléshez használt gombot. A gombnak a pirosra kell állítania (nem azonnal), és adja meg a gyalogosoknak az időtartamát, mielőtt áthelyezi a fényeket zöldre, amíg a gombot újra megnyomja.

5. Most próbáljon meg egy hangjelzést a csipogásra gyorsan jelezni, hogy biztonságos a kereszteződés, a látássérült gyalogosok javára.