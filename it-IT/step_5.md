## Sequenza dei semafori

Oltre a controllare l'insieme delle luci insieme, puoi anche controllare ciascun LED individualmente. Con i semafori a LED, un pulsante e un cicalino, puoi creare la tua sequenza di semafori, completa di passaggio pedonale!

1. Modifica il tuo loop per eseguire una sequenza automatica di LED accesi:
    
    ```python
while True: lights.green.on () sleep (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

2. Aggiungi un `wait_for_press ()` in modo che premendo il pulsante si avvii la sequenza:
    
    ```python
while True: button.wait_for_press () lights.green.on () sleep (1) lights.amber.on () sleep (1) lights.red.on () sleep (1) lights.off ()
```

Prova altre sequenze di tua scelta.

3. Ora prova a creare la sequenza completa dei semafori:
    
    - Verde acceso
    - Ambra
    - Rosso acceso
    - Rosso e ambra
    - Verde acceso
    
    Assicurati di accendere e spegnere le luci corrette al momento giusto, e assicurati di usare `sleep` per sincronizzare perfettamente la sequenza.

4. Prova ad aggiungere il pulsante per un passaggio pedonale. Il pulsante dovrebbe spostare le luci in rosso (non immediatamente) e dare ai pedoni il tempo di attraversare prima di riportare le luci in verde finché il pulsante non viene premuto di nuovo.

5. Ora prova ad aggiungere un cicalino per emettere rapidamente un segnale acustico per indicare che è sicuro attraversarlo, a beneficio dei pedoni ipovedenti.