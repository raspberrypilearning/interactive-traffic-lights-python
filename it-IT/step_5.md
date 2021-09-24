## La sequenza del semaforo

Oltre a poter controllare le luci tutte allo stesso tempo, puoi anche controllare ciascun LED individualmente. Con i LED del semaforo, un pulsante e un cicalino, puoi creare la tua sequenza, completa di un passaggio pedonale!

Prova altre sequenze a tuo piacimento.

Modifica il ciclo in modo da accendere automaticamente i LED:

```python
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

\--- /task \---

\--- task \---

Add a `wait_for_press()` so that pressing the button initiates the sequence:

```python
Aggiungi un `wait_for_press()` in modo tale che la sequenza venga avviata alla pressione del pulsante:

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

Try some more sequences of your own.

\--- /task \---

\--- task \---

Ora prova a creare la sequenza completa dei semafori:

- Verde acceso
- Giallo acceso
- Rosso acceso
- Rosso e giallo accesi
- Verde acceso

Assicurati di accendere e spegnere le luci corrette al momento giusto, e assicurati di usare `sleep` per sincronizzare perfettamente la sequenza.

\--- /task \---

\--- task \---

Prova ad aggiungere il pulsante per simulare un passaggio pedonale. Il pulsante dovrebbe spostare far diventare rosso il semaforo (non immediatamente) e dare ai pedoni il tempo di attraversare prima di far diventare di nuovo verde e finché il pulsante non viene premuto nuovamente.

\--- /task \---

\--- task \---

Ora prova ad aggiungere un cicalino per emettere un segnale acustico per segnalare che è sicuro attraversare la strada, a beneficio dei pedoni ipovedenti.

```python
buzzer = Buzzer(15)

buzzer.on()
buzzer.off()
buzzer.beep(0.1, 0.1)
```

\--- /task \---

Your final interactive traffic lights code should start on a green light and then:

- Wait for the button to be pressed
- When pressed, change to red/amber, then green
- Beep for a while to say it's time to cross
- Go to amber and then green
- Repeat