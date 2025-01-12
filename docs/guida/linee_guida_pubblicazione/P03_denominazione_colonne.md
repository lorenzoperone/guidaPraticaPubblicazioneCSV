---
hide:
 - toc
title: Denominazione delle colonne
---

# Denominazione delle colonne

I nomi dei campi o delle colonne in una tabella di dati devono essere comprensibili alle persone.

Da prendere in considerazione:

- In molti casi, le colonne delle tabelle di dati mantengono i nomi assegnati dai sistemi di gestione delle banche dati, di solito soggetti a convenzioni tecniche che sono difficili da capire per le persone.
- Alcune raccomandazioni per i nomi dei campi:
    - Non ripetere i nomi dei campi, che siano univoci.
    - Usare nomi brevi (non più di 20 caratteri) ma tenendo sempre presente che il risparmio di caratteri non deve portare a un'errata interpretazione del nome del campo.
    - Evitare di usare abbreviazioni.
    - Usare solo caratteri ASCII minuscoli (a-z; 0-9)
    - Non usare caratteri speciali (per esempio äüöàéèê, ecc.).
    - Non includere accenti o segni di punteggiatura.
    - Usare i trattini bassi `_` per separare le parole che compongono i nomi delle colonne invece degli spazi bianchi.
    - Evitare l'uso di codici, e se assolutamente necessario, dovrebbe essere spiegato nel [dizionario dei dati](../dizionario_dati.md) che documenta il set di dati.
    - I nomi dei campi devono corrispondere a quelli specificati nel dizionario dei dati.

**Esempio**: nomi comprensibili delle colonne

!!! failure "Cattiva prassi"

    |Identificatore_M|Anno|Cil.|Consumo_per_100_k<br>ms_di_viaggio_urbano|HP|m/sec^2|
    |---|---|---|---|----|----|
    |chevrolet chevelle malibu|1970|8|18|130|12|
    |buick skylark 320|1970|8|15|165|11.5|
    |plymouth satellite|1970|8|18||150|11|

!!! success "Buona prassi"

    |marca|anno|cilindri|consumo|potenza|accelerazione|
    |---|---|---|---|----|----|
    |chevrolet chevelle malibu|1970|8|18|130|12|
    |buick skylark 320|1970|8|15|165|11.5|
    |plymouth satellite|1970|8|18|150|11|

Se c'è un'entità che è definita da diverse caratteristiche separate in diversi campi, è conveniente iniziare a nominare i campi con quell'entità e poi con gli attributi più specifici (dal più generale al più specifico). Per esempio:

|cliente_nome|cliente_addebito|richiedente_tipo_documento|richiedente_numero_documento|
|---|---|---|---|
| ... | ... | ... | ... |

I campi che sono identificatori possono includere il suffisso `_id` nel nome del campo, tranne in casi eccezionali in cui un nome alternativo è più conveniente, perché fornisce informazioni sul sistema di identificazione usato.

Per i campi che contengono la descrizione di quell'identificatore, si raccomanda di includere il suffisso `_nome`, a meno che non ci sia un modo più conveniente per nominare il campo.

|rivenditore_id|rivenditore_nome|
|---|---|
| ... | ... |

