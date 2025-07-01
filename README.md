# Dataset, modelli e risultati sperimentali - CSE-CIC-IDS2018

Questa repository contiene i **file generati e utilizzati** durante la sperimentazione sul dataset CSE-CIC-IDS2018 per la tesi di laurea triennale:  
**"IDENTIFICAZIONE DI ATTACCHI WEB CON INTELLIGENZA ARTIFICIALE"** di Veronica Tavazzi (12247A).

Il materiale fornito documenta in modo completo il flusso operativo seguito per costruire e valutare un sistema di rilevamento automatico delle intrusioni su traffico di rete realistico, utilizzando il dataset **CSE-CIC-IDS2018**.  
La sperimentazione si è focalizzata sulla classificazione binaria (tra traffico benigno e malevolo), ma include anche un’analisi dettagliata per categoria di attacco.

---

## Struttura della repository

### Report di preprocessing e sperimentazione

| File                                 | Descrizione                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| `report_file_originali.txt`         | Report riepilogativo dei file CSV originali (contenuto, dimensioni, encoding) |
| `report_file_uniformati.txt`  | Descrive la pulizia, correzione e generazione dei file intermedi           |
| `report_file_preprocessati.txt`     | Dettaglio dei file generati dopo normalizzazione, encoding e bilanciamento. Inoltre, contiene l'nalisi esplorativa dei file preprocessati (distribuzioni, classi) |
| `report_file_merge.txt`                 | Fasi di unione e riorganizzazione dei dati preprocessati                   |
| `report_sottoinsiemi.txt`           | Descrizione della suddivisione in train, validation e test                 |
| `report_smote_rfe.txt`      | Report sulle tecniche di bilanciamento e selezione feature (SMOTE, RFE)   |

### Modelli addestrati

| File                         | Descrizione                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| `CIC_random_forest_model.pkl`| Modello Random Forest addestrato sul dataset CSE-CIC-IDS2018               |
| `CIC_svm_model.pkl`          | Modello SVM con kernel approssimato Nyström                                |
| `CIC_dnn_model.h5`           | Modello Deep Neural Network in formato HDF5                                |

### Risultati finali

| File                         | Descrizione                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| `CIC_random_forest_results.txt`| Metriche ottenute dal modello Random Forest                             |
| `CIC_svm_results.txt`        | Metriche ottenute dal modello SVM                                          |
| `CIC_dnn_results.txt`        | Metriche ottenute dal modello Deep Neural Network                          |

---

## Note metodologiche

A differenza della sperimentazione UNSW-NB15, per il dataset **CSE-CIC-IDS2018** non è stato possibile includere i file `.csv` completi a causa della loro dimensione elevata.  
Sono stati pertanto forniti **report testuali completi**, che descrivono nel dettaglio tutte le fasi di elaborazione, dalla pulizia iniziale alla suddivisione del dataset.

Tutti i file `.pkl` e `.h5` contengono i modelli addestrati esattamente secondo le configurazioni documentate in tesi.  
I file `.txt` riportano le metriche principali (accuracy, precision, recall, F1-score) in forma testuale e sono direttamente coerenti con le confusion matrix riportate nel Capitolo 3.

---

## Disclaimer

Il contenuto di questa repository è stato pubblicato esclusivamente per **fini accademici e documentali**.  
Tutti i file inclusi rappresentano il lavoro originale svolto per la redazione della tesi di laurea e sono resi disponibili **unicamente a titolo consultativo**.  
È espressamente vietata qualsiasi forma di **replicazione, distribuzione o utilizzo per scopi diversi da quelli di verifica accademica**.
