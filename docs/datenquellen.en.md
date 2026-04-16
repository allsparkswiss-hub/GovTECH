# Data Sources

## Principle

Only **publicly available data sources and documents** are allowed. Teams may use the examples listed below or select other suitable public sources. What matters is that origin, access path, and retrieval date are documented cleanly.

!!! warning "Mandatory minimum requirement"
    Every source used must be documented at least with **URL, format, access path, and retrieval date**. Official APIs or official downloads should be preferred over scraping.

## Example sources

| Source | Type | Typical access | Example use |
| --- | --- | --- | --- |
| [opendata.swiss](https://opendata.swiss/) / CKAN API | open government data portal | CKAN API, CSV, JSON, files | cross-domain administrative and specialist data |
| [BFS / data.bfs.admin.ch](https://www.data.bfs.admin.ch/) / PX-Web API | statistics | PX-Web API, JSON, tables | demography, economy, society, geography |
| [geo.admin.ch](https://www.geo.admin.ch/) / technical services | geodata and geoservices | WMS, WMTS, vector tiles, downloads, technical documentation | mapping context, layers, georeferencing |
| [MeteoSwiss Open Data](https://opendatadocs.meteoswiss.ch/) / STAC | weather and climate data | STAC, raster, measurement series, downloads | climate, weather trends, exposure |
| [Swiss Parliament Open Data](https://ws-old.parlament.ch/) / web services | politics and parliamentary activity | web services, structured queries | motions, debates, political signals |
| [Fedlex SPARQL](https://www.fedlex.admin.ch/de/) | law and regulation | SPARQL endpoint | regulatory change, legal context, amendments |
| [LINDAS SPARQL](https://lindas.admin.ch/) | linked open data | SPARQL endpoint | linking and semantic references |
| [Swiss Federal Office of Energy](https://www.bfe.admin.ch/bfe/de/home/versorgung/statistik-und-geodaten.html) | energy and supply statistics | official statistics, downloads, some APIs | energy supply, consumption, infrastructure indicators |

## Selection guidance

- Both structured and unstructured public sources may be used.
- Official sources should be preferred over unofficial mirrors or replicas.
- If documents, news, or studies are included, their origin should remain clear and durably referenceable.
- Sources should fit together thematically and support meaningful indicators or weak signals.

## Recommended source documentation fields

| Field | Description |
| --- | --- |
| Source | name of the organization or platform |
| URL | unique link to the source or dataset |
| Format | e.g. API, CSV, JSON, GeoJSON, PDF, SPARQL, STAC |
| Access path | concrete endpoint, download path, or query route |
| Retrieval date | date of the actual data retrieval |
| License or terms of use | document when available |
| Geographic reference | Switzerland, canton, municipality, raster, point data, etc. |
| Update logic | static, periodic, near real-time, or unknown |

## Recommendation for teams

Start with a small, well-documented source mix. A strong setup often combines:

- one or two structured official datasets
- at least one spatial source
- at least one source for textual or regulatory signals

That creates a robust MVP with a visible evidence chain instead of an overly broad integration effort.
