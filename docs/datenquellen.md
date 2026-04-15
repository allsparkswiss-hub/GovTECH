# Datenquellen

## Grundsatz

Zulässig sind ausschließlich **öffentlich verfügbare Datenquellen und Dokumente**. Teams können die unten genannten Beispiele nutzen oder andere geeignete öffentliche Quellen auswählen. Entscheidend ist, dass Herkunft, Zugriff und Abrufzeitpunkt sauber dokumentiert werden.

!!! warning "Verbindliche Mindestanforderung"
    Jede verwendete Quelle muss mindestens mit **URL, Format, Zugriffspfad und Abrufdatum** dokumentiert werden. Bevorzugt werden offizielle APIs oder offizielle Downloads statt Scraping.

## Beispielquellen

| Quelle | Typ | Typischer Zugang | Beispielhafter Nutzen |
| --- | --- | --- | --- |
| [opendata.swiss](https://opendata.swiss/) / CKAN API | Open-Government-Data-Portal | CKAN API, CSV, JSON, Dateien | Themenübergreifende Verwaltungs- und Fachdaten |
| [BFS / data.bfs.admin.ch](https://www.data.bfs.admin.ch/) / PX-Web API | Statistik | PX-Web API, JSON, Tabellen | Demografie, Wirtschaft, Gesellschaft, Raumbezug |
| [geo.admin.ch](https://www.geo.admin.ch/) / technische Dienste | Geodaten und Geoservices | WMS, WMTS, Vector Tiles, Downloads, technische Dokumentation | Kartenbezug, Layer, Georeferenzierung |
| [MeteoSwiss Open Data](https://opendatadocs.meteoswiss.ch/) / STAC | Wetter- und Klimadaten | STAC, Raster, Messreihen, Downloads | Klima, Wettertrends, Exposition |
| [Swiss Parliament Open Data](https://ws.parlament.ch/) / Web Services | Politik und parlamentarische Aktivität | Web Services, strukturierte Abfragen | Vorstösse, Debatten, politische Signale |
| [Fedlex SPARQL](https://www.fedlex.admin.ch/de/home/sparql.html) | Recht und Regulierung | SPARQL Endpoint | Regulierungsentwicklung, Normbezug, Rechtsänderungen |
| [LINDAS SPARQL](https://lindas.admin.ch/) | Linked Open Data | SPARQL Endpoint | Verknüpfung und semantische Referenzen |
| [Schweizerisches Bundesamt für Energie](https://www.bfe.admin.ch/bfe/de/home/versorgung/statistik-und-geodaten.html) | Energie- und Versorgungsstatistik | offizielle Statistiken, Downloads, teils APIs | Energieversorgung, Verbrauch, Infrastrukturindikatoren |

## Hinweise zur Auswahl

- Wählbar sind strukturierte und unstrukturierte öffentliche Quellen.
- Offizielle Quellen sind gegenüber inoffiziellen Replikaten zu bevorzugen.
- Wenn Dokumente, News oder Studien eingebunden werden, sollte die Herkunft klar und dauerhaft referenzierbar sein.
- Quellen sollten thematisch zusammenpassen und sich sinnvoll auf Indikatoren oder Weak Signals beziehen lassen.

## Empfohlene Dokumentation pro Quelle

| Feld | Beschreibung |
| --- | --- |
| Quelle | Name der Organisation oder Plattform |
| URL | eindeutiger Link zur Quelle oder zum Datensatz |
| Format | z. B. API, CSV, JSON, GeoJSON, PDF, SPARQL, STAC |
| Zugriffspfad | konkreter Endpoint, Downloadpfad oder Abfrageweg |
| Abrufdatum | Datum des verwendeten Datenabrufs |
| Lizenz oder Nutzungsbedingung | falls verfügbar dokumentieren |
| Geografischer Bezug | Schweiz, Kanton, Gemeinde, Raster, Punktdaten etc. |
| Aktualisierungslogik | statisch, periodisch, near-real-time oder unbekannt |

## Empfehlung für Teams

Startet mit einem kleinen, gut dokumentierten Quellenmix. Ein gutes Setup kombiniert oft:

- eine oder zwei strukturierte amtliche Datenquellen
- mindestens eine raumbezogene Quelle
- mindestens eine Quelle für textuelle oder regulatorische Signale

So entsteht früh ein belastbarer MVP mit sichtbarer Evidenzkette statt einer schwer beherrschbaren Integrationsbreite.
