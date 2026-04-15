# Architektur

## Zielbild

Die Challenge eignet sich für eine modulare, schichtartige Architektur. Sie trennt Quellenanbindung, Verarbeitung, Speicherung, Analyse, Bereitstellung und Dokumentation sauber voneinander. Das erleichtert Nachvollziehbarkeit, Austauschbarkeit einzelner Komponenten und spätere Weiterentwicklung nach dem Hackathon.

![Architekturübersicht](assets/architecture-overview.svg)

## Layered Architecture im Ueberblick

| Layer | Aufgabe | Typische Ergebnisse |
| --- | --- | --- |
| Source Layer | Öffentliche Datenquellen, Dokumente und Services anbinden | Rohdaten, Metadaten, Quellreferenzen |
| Ingestion Layer | Abruf, Download, Connector-Logik und technische Erfassung | API-Antworten, Dateien, Snapshots |
| Raw Data Layer | Unveränderte Ablage der Quellartefakte | versionierte Originaldaten und Abrufprotokolle |
| Processing / ETL / ELT Layer | Parsing, Bereinigung, Normalisierung und Mapping | harmonisierte Datensätze und abgeleitete Merkmale |
| Storage Layer | strukturierte Ablage für Analyse und Wiederverwendung | relationale Tabellen, Geodaten, optionale Dokument- oder Vektorspeicher |
| Analytics & Intelligence Layer | Indikatoren, Trendkarten, Weak Signals und Evidenzlogik | berechnete Kennzahlen, Signale, Bewertungen |
| API Layer | standardisierte Bereitstellung für Frontend oder Drittsysteme | REST-Endpunkte, OpenAPI, Swagger UI |
| Presentation Layer | Dashboard, Web-App und Visualisierung | Karten, Zeitachsen, Indikatoren, Filter |
| Documentation Layer | technische und fachliche Nachvollziehbarkeit | Quelleninventar, Architektur, Reproduzierbarkeit |

## Architekturprinzipien

- **Modularität:** jede Schicht soll austauschbar und separat testbar bleiben
- **Quellentransparenz:** jedes Ergebnis bleibt auf konkrete Quellen referenzierbar
- **Versionierung:** Rohdaten, Transformationslogik und Indikatoren sollen nachvollziehbar versioniert sein
- **Reproduzierbarkeit:** Doku, Schema und Zugriffslogik müssen nach dem Hackathon wiederverwendbar sein
- **Kleiner Kern:** lieber wenige tragfähige Komponenten als ein zu breiter Stack ohne Betriebsreife

## Technologische Leitplanken

| Bereich | Empfehlung |
| --- | --- |
| SQL-Datenbank | **PostgreSQL** als bevorzugte relationale Basis |
| Geodaten | **PostGIS** optional für raumbezogene Analysen |
| Dokument- oder NoSQL-Speicher | **MongoDB** optional |
| Vector Store | **ChromaDB** optional |
| Suche / Volltext | optionale Suchdatenbank für Keyword- oder Volltextsuche |
| Backend / API | **FastAPI** |
| Frontend | **React** oder **Streamlit** |
| Dokumentation | **MkDocs** |
| API-Dokumentation | **Swagger UI / OpenAPI** |

## Minimaler technischer Zuschnitt für ein MVP

Ein pragmatischer MVP kann bereits mit folgenden Bausteinen funktionieren:

- Connectoren für 4 öffentliche Quellen
- Rohdatenablage plus einfache Versionierung
- PostgreSQL als zentrale Arbeitsdatenbank
- FastAPI für Daten- und Indikatorbereitstellung
- React- oder Streamlit-Frontend mit Karte und Zeitachse
- MkDocs für technische und fachliche Dokumentation

!!! note "Pragmatischer Fokus"
    Nicht jede optionale Komponente muss im Hackathon umgesetzt werden. Entscheidend ist, dass der Gesamtfluss von der Quelle bis zur Visualisierung nachvollziehbar funktioniert.
