<!-- ELUCENIA technical documentation · das28 · it · no clinical/professional/rights approval -->

# DAS28 (VES e PCR)

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/das28)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Articolazioni dolenti (su 28)

`tjc`

intervallo: 0–28

### Articolazioni tumefatte (su 28)

`sjc`

intervallo: 0–28

### Valutazione globale della salute del paziente (scala visiva)

`gh`

mm · intervallo: 0–100

### Velocità di eritrosedimentazione (VES)

`vhs`

mm/h · facoltativo · intervallo: 1–150

### Proteina C-reattiva (PCR)

`pcr`

mg/L · facoltativo · intervallo: 0–300

## Edizione del metodo

DAS28-VES/Prevoo 1995 e DAS28-PCR/Wells 2009; 28 articolazioni; intercetta PCR 0,96

## Formula documentata

DAS28-VES = 0,56 × √(dolenti) + 0,28 × √(tumefatte) + 0,70 × ln(VES) + 0,014 × valutazione globale.

DAS28-PCR = 0,56 × √(dolenti) + 0,28 × √(tumefatte) + 0,36 × ln(PCR + 1) + 0,014 × valutazione globale + 0,96 (PCR in mg/L).

## Limiti e popolazione

Il DAS28 del 1995 è stato sviluppato per l’attività dell’artrite reumatoide, usando il conteggio di 28 articolazioni e confronti con la valutazione clinica dei reumatologi. La variante con PCR non è automaticamente equivalente a quella con VES; formula, unità e soglie devono corrispondere alla fonte e all’edizione utilizzate.

## Riferimenti

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

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

Attività moderata dell’artrite reumatoide


### 2

Remissione dell’artrite reumatoide


### 3

Alta attività dell’artrite reumatoide


### 4

Attività moderata dell’artrite reumatoide

Il DAS28-CRP di solito dà valori inferiori al DAS28-VES: con gli stessi cut-off, la remissione può essere sovrastimata.

