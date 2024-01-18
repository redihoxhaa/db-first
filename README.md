# DB AUTO USATE

#### CONSEGNA DELL'ESERCIZIO 

```
Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario.
```

#### SVOLGIMENTO

Componia la nostra tabella in questo modo:

1. **ID**: INT, PK (NOT NULL, AUTO_INCREMENT, UNIQUE). È la chiave primaria della tabella e identifica univocamente ogni auto, dato obbligatorio autoincrementale, limite numerico a 4.294.967.295 (siamo ottimisti).
2. **Marca**: VARCHAR(50), NOT NULL. Rappresenta la marca dell'auto, limite di 50 caratteri, dato obbligatorio.
3. **Modello**: VARCHAR(50), NOT NULL. Indica il modello dell'auto, limite di 50 caratteri, dato obbligatorio.
4. **Anno**: YEAR, NOT NULL. L'anno di produzione dell'auto, formattazione YYYY, dato obbligatorio.
5. **Prezzo**: DECIMAL(10,2), NOT NULL. Il prezzo di vendita dell'auto, massimo importo 99.999.999,99, dato obbligatorio.
6. **Chilometraggio**: MEDIUMINT, NOT NULL. Il chilometraggio dell'auto, massimo chilometraggio 16.777.215, dato obbligatorio.
7. **Colore**: VARCHAR(30), NULL. Il colore dell'auto, limite di 30 caratteri, dato opzionale.
8. **Alimentazione**: VARCHAR(20), NOT NULL. Il tipo di carburante utilizzato dall'auto, limite di 20 caratteri, dato obbligatorio.
9. **Stato veicolo**: VARCHAR(100), NULL. Descrive lo stato del veicolo, limite di 100 caratteri, dato opzionale.
10. **N° precedenti proprietari**: TINYINT, NULL. Indica il numero dei precedenti proprietari del veicolo, limite a 255, dato opzionale.
11. **Data inserimento**: DATETIME, DEFAULT (CURRENT DATETIME). La data e l'ora in cui l'auto è stata inserita nel database, di default è la data e l'ora attuale in formato YYYY-MM-DD HH:II:SS.