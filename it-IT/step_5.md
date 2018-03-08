## La sequenza del semaforo

Oltre a poter controllare le luci tutte allo stesso tempo, puoi anche controllare ciascun LED individualmente. Con i LED del semaforo, un pulsante e un cicalino, puoi creare la tua sequenza, completa di un passaggio pedonale!

1. Modifica il ciclo in modo da accendere automaticamente i LED:
    
    ```python
while True:
    lights.green.on()
    sleep(1)
    lights.amber.on()
    sleep(1)
    lights.red.on()
    sleep(1)
    lights.off()
```

2. Aggiungi un `wait_for_press()` in modo tale che la sequenza venga avviata alla pressione del pulsante:
    
    ```python
while True:
    button.wait_for_press()
    lights.green.on()
    sleep(1)
    lights.amber.on()
    sleep(1)
    lights.red.on()
    sleep(1)
    lights.off()
```

Prova altre sequenze a tuo piacimento.

3. Ora prova a creare la sequenza completa dei semafori:
    
    - Verde acceso
    - Ambra
    - Rosso acceso
    - Rosso e ambra
    - Verde acceso
    
    Assicurati di accendere e spegnere le luci corrette al momento giusto, e assicurati di usare `sleep` per sincronizzare perfettamente la sequenza.

4. Prova ad aggiungere il pulsante per simulare un passaggio pedonale. Il pulsante dovrebbe spostare far diventare rosso il semaforo (non immediatamente) e dare ai pedoni il tempo di attraversare prima di far diventare di nuovo verde e finché il pulsante non viene premuto nuovamente.

5. Ora prova ad aggiungere un cicalino per emettere un segnale acustico per segnalare che è sicuro attraversare la strada, a beneficio dei pedoni ipovedenti.