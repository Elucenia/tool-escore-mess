<!-- ELUCENIA technical documentation · escore-mess · it · no clinical/professional/rights approval -->

# MESS (punteggio di gravità dell’arto gravemente lesionato)

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/escore-mess)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Lesione scheletrica e dei tessuti molli

`energia`

- `1` — Bassa energia (ferita da arma bianca, frattura semplice, proiettile di arma corta)
- `2` — Energia media (frattura esposta o multipla, lussazione)
- `3` — Alta energia (incidente ad alta velocità, proiettile di fucile)
- `4` — Energia molto alta (quanto sopra + contaminazione grossolana)

### Ischemia dell’arto

`isquemia`

- `0` — Senza ischemia
- `1` — Polso ridotto o assente, perfusione normale
- `2` — Assenza di polso, parestesie, riempimento capillare lento
- `3` — Arto freddo, paralizzato, insensibile

### Ischemia da più di 6 ore?

`tempo`

- `0` — No
- `1` — Sì

### Shock

`choque`

- `0` — Pressione arteriosa sistolica sempre \> 90 mmHg
- `1` — Ipotensione transitoria
- `2` — Ipotensione persistente

### Età

`idade`

- `0` — \< 30 anni
- `1` — 30 a 50 anni
- `2` — \> 50 anni

## Edizione del metodo

MESS/Johansen 1990: 4 domini, ischemia raddoppiata \>6 h; nessun ordine automatico di amputazione

## Formula documentata

MESS = lesione scheletrica/tessuti molli (1–4) + ischemia (0–3, raddoppiata se dura oltre 6 h) + shock (0–2) + età (0–2).

## Limiti e popolazione

Il MESS originale è stato derivato in piccoli gruppi con trauma grave dell’arto inferiore. L’associazione della soglia ≥7 con l’amputazione in tali gruppi non stabilisce una regola universale o un’indicazione automatica. Il salvataggio dell’arto dipende dalla valutazione multidisciplinare e da condizioni cliniche non riassunte nel punteggio.

## Riferimenti

- [Johansen K et al. Objective criteria accurately predict amputation following lower extremity trauma. J Trauma, 1990.](https://doi.org/10.1097/00005373-199005000-00007)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

MESS < 7: intervallo di salvataggio dell’arto nella serie originale

| Dettagli del risultato | |
| --- | --- |
| Punti di ischemia | 1 |

Il MESS non decide da solo: l’indicazione all’amputazione primaria spetta al team (ortopedia, vascolare e plastica), con il paziente stabilizzato.


### 2

MESS ≥ 7: nella serie originale, tutti gli arti con questo punteggio sono stati amputati

| Dettagli del risultato | |
| --- | --- |
| Punti di ischemia | 4 (raddoppiati: ischemia > 6 h) |

Il MESS non decide da solo: l’indicazione all’amputazione primaria spetta al team (ortopedia, vascolare e plastica), con il paziente stabilizzato.


### 3

MESS ≥ 7: nella serie originale, tutti gli arti con questo punteggio sono stati amputati

| Dettagli del risultato | |
| --- | --- |
| Punti di ischemia | 2 |

Il MESS non decide da solo: l’indicazione all’amputazione primaria spetta al team (ortopedia, vascolare e plastica), con il paziente stabilizzato.

