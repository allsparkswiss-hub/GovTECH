# Fonti di dati

## Principio

Sono ammesse esclusivamente **fonti di dati e documenti pubblicamente disponibili**. I team possono usare gli esempi sotto indicati oppure scegliere altre fonti pubbliche adatte. L’importante è documentare in modo chiaro origine, percorso di accesso e data di acquisizione.

!!! warning "Requisito minimo obbligatorio"
    Ogni fonte utilizzata deve essere documentata almeno con **URL, formato, percorso di accesso e data di acquisizione**. Sono da preferire API ufficiali o download ufficiali rispetto allo scraping.

## Esempi di fonti

| Fonte | Tipo | Accesso tipico | Possibile utilizzo |
| --- | --- | --- | --- |
| [opendata.swiss](https://opendata.swiss/) / CKAN API | portale open government data | CKAN API, CSV, JSON, file | dati amministrativi e specialistici trasversali |
| [BFS / data.bfs.admin.ch](https://www.data.bfs.admin.ch/) / PX-Web API | statistiche | PX-Web API, JSON, tabelle | demografia, economia, società, geografia |
| [geo.admin.ch](https://www.geo.admin.ch/) / servizi tecnici | geodati e geoservizi | WMS, WMTS, vector tiles, download, documentazione tecnica | contesto cartografico, layer, georeferenziazione |
| [MeteoSwiss Open Data](https://opendatadocs.meteoswiss.ch/) / STAC | dati meteo e climatici | STAC, raster, serie di misura, download | clima, trend meteorologici, esposizione |
| [Swiss Parliament Open Data](https://ws-old.parlament.ch/) / web services | politica e attività parlamentare | web services, query strutturate | mozioni, dibattiti, segnali politici |
| [Fedlex SPARQL](https://www.fedlex.admin.ch/de/) | diritto e regolazione | endpoint SPARQL | evoluzione normativa, contesto giuridico, modifiche |
| [LINDAS SPARQL](https://lindas.admin.ch/) | linked open data | endpoint SPARQL | collegamenti e riferimenti semantici |
| [Ufficio federale svizzero dell’energia](https://www.bfe.admin.ch/bfe/de/home/versorgung/statistik-und-geodaten.html) | statistiche energia e approvvigionamento | statistiche ufficiali, download, in parte API | approvvigionamento energetico, consumi, indicatori infrastrutturali |

## Indicazioni per la selezione

- Possono essere utilizzate fonti pubbliche strutturate e non strutturate.
- Le fonti ufficiali sono da preferire a mirror o repliche non ufficiali.
- Se si integrano documenti, news o studi, la loro origine deve restare chiara e durevolmente referenziabile.
- Le fonti dovrebbero essere coerenti sul piano tematico e supportare indicatori o weak signals significativi.

## Documentazione raccomandata per ogni fonte

| Campo | Descrizione |
| --- | --- |
| Fonte | nome dell’organizzazione o della piattaforma |
| URL | link univoco alla fonte o al dataset |
| Formato | ad es. API, CSV, JSON, GeoJSON, PDF, SPARQL, STAC |
| Percorso di accesso | endpoint concreto, percorso di download o query |
| Data di acquisizione | data effettiva del recupero |
| Licenza o condizioni d’uso | documentare se disponibili |
| Riferimento geografico | Svizzera, cantone, comune, raster, punti ecc. |
| Logica di aggiornamento | statica, periodica, near-real-time o sconosciuta |

## Raccomandazione per i team

Partite con un mix ristretto ma ben documentato di fonti. Un setup solido combina spesso:

- una o due fonti ufficiali strutturate
- almeno una fonte spaziale
- almeno una fonte per segnali testuali o regolatori

In questo modo si ottiene rapidamente un MVP robusto con una catena di evidenza visibile, invece di un’integrazione troppo ampia e difficile da gestire.
