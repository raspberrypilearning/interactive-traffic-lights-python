## La sequenza del semaforo

Oltre a poter controllare le luci tutte allo stesso tempo, puoi anche controllare ciascun LED individualmente. Con i LED del semaforo, un pulsante e un cicalino, puoi creare la tua sequenza, completa di un passaggio pedonale!

\--- task \---

Modifica il ciclo in modo da accendere autonomamente i LED:

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

Prova altre sequenze a tuo piacimento.

\--- /task \---

\--- task \---

Ora prova a creare la sequenza completa del semaforo:

- Verde attivato
- Giallo attivato
- Rosso attivato
- Rosso e giallo attivati
- Verde attivato

Assicurati di accendere e spegnere le luci corrette al momento giusto e assicurati di usare `sleep` per sincronizzare perfettamente la sequenza.

\--- /task \---

\--- task \---

Prova ad aggiungere il pulsante per simulare un passaggio pedonale. Il pulsante dovrebbe far diventare rosso il semaforo (non immediatamente) e dare ai pedoni il tempo di attraversare prima di farlo diventare nuovamente verde finché il pulsante non verrà premuto nuovamente.

\--- /task \---

\--- task \---

Ora prova ad aggiungere un cicalino per emettere un segnale acustico per segnalare che è sicuro attraversare la strada, a beneficio dei pedoni ipovedenti:

```python
buzzer = Buzzer (15)

buzzer.on ()
buzzer.off ()
buzzer.beep (0.1, 0.1)
```

\--- /task \---

Il codice finito del tuo semaforo interattivo dovrebbe iniziare con una luce verde e quindi:

- Attendere che il pulsante venga premuto
- Quando premuto, cambia in rosso/giallo, quindi verde
- Emettere un suono per un po' per informare che è tempo di attraversare
- Passare al giallo e poi al verde
- Ripetere