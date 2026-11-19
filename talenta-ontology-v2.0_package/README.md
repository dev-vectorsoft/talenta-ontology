# Talenta Ontology for Digital Twin Asset Management – v2.0

> **Release status: Approved for publication.**

## Purpose

The Talenta ontology provides a shared semantic model of transport infrastructure assets for digital-twin–based asset management. It was developed in the mFUND project **Talenta** (grant number / Förderkennzeichen 01F2235A–C, 01.01.2023–31.10.2025). The project title was *Intelligente Asset-Management-Plattform für digitale Zwillinge mittels Knowledge-Graph und maschinellen Lernens zur automatischen semantischen Auswertung und Verlinkung heterogener Daten aus der physischen Welt*.

The ontology links three kinds of information in one knowledge graph:

- **Asset descriptions**: transport infrastructure (road, railway, railway sleeper, bridge, tunnel, airport) and vehicles (land vehicles, aircraft, watercraft).
- **Bridge information**: bridge components, building materials and structural assessment, aligned with the German road bridge vocabulary (ASB-ING terms such as *Bauwerksname*, *JaSt-Lage*, *Sachverhalt*).
- **Operational and observation data**: public-transport timetables (GTFS vocabulary), sensors and observations (SOSA/SSN), time (OWL-Time), geometry and location (GeoSPARQL, UTM32N coordinates) and units of measure.

## Intended use

- Semantic integration of heterogeneous asset data (tabular, JSON/XML, text, geometry) into a knowledge graph.
- Linking timetable and delay data (GTFS) to infrastructure assets, for example together with the companion sample dataset.
- A starting point for asset-management applications, search over asset knowledge graphs, and explainable-AI analytics on infrastructure data.

This release is a research prototype. It has not been validated for operational or safety-relevant use.

## Files

| File | Content |
|---|---|
| `talenta-ontology-v2.0.rdf` | The ontology in RDF/XML (OWL 2). This is the authoritative release file. It is identical to the project file `ontology.rdf` (SHA-256 in `SHA256SUMS.txt`). |
| `talenta-ontology-v2.0.ttl` | The same graph in Turtle (8,279 triples), converted with rdflib 7.6. Provided for convenience. |
| `examples/queries.rq` | Five example SPARQL queries. |
| `examples/queries_test_result.txt` | Result row counts from the test run. |
| `THIRD_PARTY_NOTICES.md` | Reused vocabularies and the license statements found in the file. |
| `ontology-header-proposal.ttl` | Proposed Talenta-specific ontology metadata, to be added before release (see "Known limitations"). |

## Structure and size

- **Ontology IRI:** `https://github.com/dev-vectorsoft/talenta/ontology`
- **Version IRI:** `https://github.com/dev-vectorsoft/talenta/ontology/2.0`
- **Talenta namespace:** `https://github.com/dev-vectorsoft/talenta/ontology#` (suggested prefix `talenta:`)

The file is a merged release: imported vocabularies are included in the file. In total it declares 387 classes, 273 object properties, 186 datatype properties and 194 named individuals.

The Talenta-specific module contains:

- 44 classes, for example:
  - `Asset`, `TransportationInfrastructure`, `Vehicle`, `BridgeInfrastructure`
  - `ConditionRating`, `MaterialProperty`, `Geolocation`, `Geometry`, `Sensor`, `Time`
- 8 object properties: `hasGeolocation`, `hasGeometry`, `hasProperty`, `hasSensor`, `hasTime`, `hasRoute`, `hasTrip`, `hasSleeper`.
- 1 datatype property: `utm32nCoordinate`.
- 79 named individuals in `…/ontology/germanroadbridge#`. Together they describe one example road bridge (piles, caps, piers, bearings, girder segments, deck) with its building materials.

## Usage

Load the file into any RDF/OWL tool, for example Protégé, Apache Jena or GraphDB, or Python rdflib:

```python
import rdflib
g = rdflib.Graph()
g.parse("talenta-ontology-v2.0.ttl", format="turtle")
print(len(g))  # 8279
```

Then run the queries in `examples/queries.rq`. The tested result counts are:

| Query | Result rows |
|---|---|
| Q1 Talenta classes | 47 |
| Q2 class hierarchy below `talenta:Asset` | 147 |
| Q3 Talenta object properties | 8 |
| Q4 bridge components and materials | 123 |
| Q5 GTFS terms | 69 |

The file still contains `owl:imports` statements. Tools that resolve imports will try to fetch the imported IRIs. The content is already included in the file, so imports can be ignored ("offline" mode).

## Companion dataset

`Talenta: Sample Dataset with Calculated Public-Transport Delays (10 Stops)` demonstrates the timetable part of the ontology (GTFS vocabulary).

- Mobilithek: [[TBD]]

## Known limitations

These are recorded for transparency. Fixing them is optional and needs a new version number.

1. **No Talenta-specific ontology header.** The `owl:Ontology` annotations in the file are the merged headers of the imported ontologies (titles, creators, licenses and dates of iCity, SOSA/SSN, OWL-Time, the WISIB bridge ontologies and others). There is no Talenta title, description, creator or license. `ontology-header-proposal.ttl` provides one.
2. **Sparse documentation.** Only 12 of the 44 Talenta classes have an `rdfs:comment`, and 6 have an `rdfs:label`.
3. **Malformed IRIs.** 4 IRIs start with `http://http://www.opengis.net/…` (GeoSPARQL).
4. **Ill-typed literals.** 2 literals do not match their datatype. One is a date written as text; the other is an IRI typed as `xsd:decimal`.

## Version, license and citation

- **Version:** 2.0 (from `owl:versionIRI`)
- **Release date:** 2026-11-20
- **License of the Talenta-specific parts:** CC BY 4.0
- **Third-party content:** all rights in the reused vocabularies remain with their respective owners. They are reused under their own license terms, which the Talenta license does not change; see `THIRD_PARTY_NOTICES.md`.
- **Data owner (Dateneigner):** Vectorsoft AG
- **Publisher / data provider:** Vectorsoft AG

**Attribution statement:**

> Talenta Ontology v2.0. mFUND project Talenta (FKZ 01F2235A–C), Vectorsoft AG, Constructor University Bremen gGmbH and Concedra GmbH, funded by the German Federal Ministry of Transport (BMV) within the mFUND program. Licensed under terms of "CC BY 4.0" (https://creativecommons.org/licenses/by/4.0/deed.de).

Contributor roles, following CRediT (https://credit.niso.org):

| Organization | Roles |
|---|---|
| Vectorsoft AG | Conceptualization, Data curation, Formal analysis, Funding acquisition, Investigation, Project administration, Resources, Software, Validation, Visualization, Writing – review & editing |
| Constructor University Bremen gGmbH | Conceptualization, Formal analysis, Funding acquisition, Investigation, Methodology, Resources, Software, Supervision, Visualization, Writing – original draft, Writing – review & editing |
| Concedra GmbH | Conceptualization, Resources, Software, Validation, Visualization |

## Documentation and contact

- **Documentation:** https://github.com/dev-vectorsoft/talenta-ontology. See also the project's final report (Schlussbericht), Teil II, Ziel 1 (AP1).
- **Technical contact:** info@vectorsoft.de
