# Architecture

## Target picture

The challenge lends itself to a modular layered architecture. It separates source connection, processing, storage, analytics, delivery, and documentation. That improves traceability, allows components to be exchanged more easily, and supports further development after the hackathon.

![Architecture overview](assets/architecture-overview.svg)

## Layered architecture at a glance

| Layer | Purpose | Typical outputs |
| --- | --- | --- |
| Source Layer | connect public data sources, documents, and services | raw data, metadata, source references |
| Ingestion Layer | retrieval, download logic, and technical capture | API responses, files, snapshots |
| Raw Data Layer | store source artifacts unchanged | versioned originals and retrieval logs |
| Processing / ETL / ELT Layer | parsing, cleaning, normalization, and mapping | harmonized datasets and derived features |
| Storage Layer | structured storage for analysis and reuse | relational tables, geodata, optional document or vector stores |
| Analytics & Intelligence Layer | indicators, trend cards, weak signals, and evidence logic | calculated metrics, signals, assessments |
| API Layer | standardized delivery for frontend or other consumers | REST endpoints, OpenAPI, Swagger UI |
| Presentation Layer | dashboard, web app, and visualization | maps, timelines, indicators, filters |
| Documentation Layer | technical and analytical traceability | source inventory, architecture, reproducibility |

## Architecture principles

- **Modularity:** every layer should remain replaceable and testable on its own
- **Source transparency:** every result should remain tied back to concrete sources
- **Versioning:** raw data, transformation logic, and indicators should be reproducibly versioned
- **Reproducibility:** documentation, schema, and access logic should remain reusable after the hackathon
- **Small core:** prefer a few reliable components over a broad but fragile stack

## Technology guidance

| Area | Recommendation |
| --- | --- |
| SQL database | **PostgreSQL** as the preferred relational base |
| Geospatial data | **PostGIS** optional for spatial analytics |
| Document or NoSQL storage | **MongoDB** optional |
| Vector store | **ChromaDB** optional |
| Search / full text | optional search database for keyword or full-text search |
| Backend / API | **FastAPI** |
| Frontend | **React** or **Streamlit** |
| Documentation | **MkDocs** |
| API documentation | **Swagger UI / OpenAPI** |

## Minimal technical cut for an MVP

A pragmatic MVP can already work with the following building blocks:

- connectors for four public sources
- raw data storage plus simple versioning
- PostgreSQL as the central working database
- FastAPI for data and indicator delivery
- React or Streamlit frontend with a map and a timeline
- MkDocs for technical and analytical documentation

!!! note "Pragmatic focus"
    Not every optional component needs to be implemented during the hackathon. What matters is that the end-to-end flow from source to visualization works in a traceable way.
