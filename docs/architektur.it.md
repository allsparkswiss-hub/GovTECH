# Architettura

## Visione d’insieme

La challenge si presta a un’architettura modulare a livelli. Separa chiaramente connessione alle fonti, elaborazione, storage, analisi, distribuzione e documentazione. Questo migliora la tracciabilità, facilita la sostituzione dei componenti e supporta l’evoluzione dopo l’hackathon.

![Panoramica dell’architettura](assets/architecture-overview.svg)

## Layered architecture in sintesi

| Layer | Ruolo | Output tipici |
| --- | --- | --- |
| Source Layer | collegare fonti dati pubbliche, documenti e servizi | dati grezzi, metadati, riferimenti di fonte |
| Ingestion Layer | recupero, download e acquisizione tecnica | risposte API, file, snapshot |
| Raw Data Layer | conservare invariati gli artefatti delle fonti | originali versionati e log di acquisizione |
| Processing / ETL / ELT Layer | parsing, pulizia, normalizzazione e mapping | dataset armonizzati e caratteristiche derivate |
| Storage Layer | storage strutturato per analisi e riuso | tabelle relazionali, geodati, store documentali o vettoriali opzionali |
| Analytics & Intelligence Layer | indicatori, trend card, weak signals e logica dell’evidenza | metriche calcolate, segnali, valutazioni |
| API Layer | distribuzione standardizzata verso frontend o altri consumer | endpoint REST, OpenAPI, Swagger UI |
| Presentation Layer | dashboard, web app e visualizzazione | mappe, timeline, indicatori, filtri |
| Documentation Layer | tracciabilità tecnica e analitica | inventario fonti, architettura, riproducibilità |

## Principi architetturali

- **Modularità:** ogni layer dovrebbe restare sostituibile e testabile separatamente
- **Trasparenza delle fonti:** ogni risultato deve restare collegato a fonti concrete
- **Versioning:** dati grezzi, logica di trasformazione e indicatori devono essere versionati in modo tracciabile
- **Riproducibilità:** documentazione, schema e logica di accesso devono restare riutilizzabili dopo l’hackathon
- **Core ridotto:** meglio pochi componenti affidabili che uno stack ampio ma fragile

## Indicazioni tecnologiche

| Area | Raccomandazione |
| --- | --- |
| Database SQL | **PostgreSQL** come base relazionale preferita |
| Geodati | **PostGIS** opzionale per analisi spaziali |
| Storage documentale o NoSQL | **MongoDB** opzionale |
| Vector store | **ChromaDB** opzionale |
| Ricerca / full text | database di ricerca opzionale per keyword o full text |
| Backend / API | **FastAPI** |
| Frontend | **React** o **Streamlit** |
| Documentazione | **MkDocs** |
| Documentazione API | **Swagger UI / OpenAPI** |

## Taglio tecnico minimo per un MVP

Un MVP pragmatico può già funzionare con questi blocchi:

- connettori per quattro fonti pubbliche
- storage dei dati grezzi con versioning semplice
- PostgreSQL come database di lavoro centrale
- FastAPI per esporre dati e indicatori
- frontend React o Streamlit con mappa e timeline
- MkDocs per documentazione tecnica e analitica

!!! note "Focus pragmatico"
    Non è necessario implementare ogni componente opzionale durante l’hackathon. Conta che il flusso end-to-end dalla fonte alla visualizzazione funzioni in modo tracciabile.
