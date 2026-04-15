# Sources de données

## Principe

Seules les **sources de données et documents publiquement disponibles** sont autorisées. Les équipes peuvent utiliser les exemples ci-dessous ou choisir d’autres sources publiques adaptées. L’essentiel est de documenter proprement l’origine, le chemin d’accès et la date de récupération.

!!! warning "Exigence minimale obligatoire"
    Chaque source utilisée doit être documentée au minimum avec **URL, format, chemin d’accès et date de récupération**. Les API officielles ou téléchargements officiels sont à privilégier par rapport au scraping.

## Exemples de sources

| Source | Type | Accès typique | Usage possible |
| --- | --- | --- | --- |
| [opendata.swiss](https://opendata.swiss/) / CKAN API | portail open government data | CKAN API, CSV, JSON, fichiers | données administratives et métier transversales |
| [BFS / data.bfs.admin.ch](https://www.data.bfs.admin.ch/) / PX-Web API | statistiques | PX-Web API, JSON, tableaux | démographie, économie, société, géographie |
| [geo.admin.ch](https://www.geo.admin.ch/) / services techniques | géodonnées et géoservices | WMS, WMTS, vector tiles, téléchargements, documentation technique | contexte cartographique, couches, géoréférencement |
| [MeteoSwiss Open Data](https://opendatadocs.meteoswiss.ch/) / STAC | données météo et climat | STAC, rasters, séries de mesures, téléchargements | climat, tendances météo, exposition |
| [Swiss Parliament Open Data](https://ws.parlament.ch/) / web services | politique et activité parlementaire | web services, requêtes structurées | interventions, débats, signaux politiques |
| [Fedlex SPARQL](https://www.fedlex.admin.ch/de/home/sparql.html) | droit et réglementation | endpoint SPARQL | évolution réglementaire, contexte juridique, modifications |
| [LINDAS SPARQL](https://lindas.admin.ch/) | linked open data | endpoint SPARQL | liens et références sémantiques |
| [Office fédéral suisse de l’énergie](https://www.bfe.admin.ch/bfe/de/home/versorgung/statistik-und-geodaten.html) | statistiques énergie et approvisionnement | statistiques officielles, téléchargements, parfois API | approvisionnement énergétique, consommation, indicateurs d’infrastructure |

## Indications pour le choix

- Les sources publiques structurées et non structurées sont possibles.
- Les sources officielles sont à privilégier par rapport aux répliques non officielles.
- Si des documents, actualités ou études sont intégrés, leur origine doit rester claire et durablement référencable.
- Les sources doivent être cohérentes sur le plan thématique et permettre des indicateurs ou weak signals utiles.

## Documentation recommandée par source

| Champ | Description |
| --- | --- |
| Source | nom de l’organisation ou de la plateforme |
| URL | lien unique vers la source ou le dataset |
| Format | p. ex. API, CSV, JSON, GeoJSON, PDF, SPARQL, STAC |
| Chemin d’accès | endpoint concret, chemin de téléchargement ou requête |
| Date de récupération | date effective du téléchargement ou de l’appel |
| Licence ou conditions d’usage | à documenter si disponible |
| Référence géographique | Suisse, canton, commune, raster, points, etc. |
| Logique de mise à jour | statique, périodique, quasi temps réel ou inconnue |

## Recommandation pour les équipes

Commencez avec un petit mélange de sources bien documentées. Un bon setup combine souvent :

- une ou deux sources officielles structurées
- au moins une source spatiale
- au moins une source pour des signaux textuels ou réglementaires

Cela permet d’obtenir rapidement un MVP solide avec une chaîne de preuve visible, plutôt qu’une intégration trop large et difficile à maîtriser.
