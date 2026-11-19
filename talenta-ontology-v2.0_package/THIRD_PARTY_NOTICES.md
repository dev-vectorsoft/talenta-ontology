# Third-party vocabularies in talenta-ontology-v2.0.rdf

The Talenta ontology reuses and includes (merges) the vocabularies below. They keep their own licenses and attribution requirements. The license statements were taken from the merged `owl:Ontology` header of the release file. The merged header does not show which statement belongs to which source vocabulary, so the "Source license" column must be checked against each original source before release.

## General notice on third-party content

This release contains or refers to vocabularies, ontologies, data models and other materials created by third parties ("third-party content"), as listed below. All rights in third-party content, including copyright, database rights and trademarks, remain with their respective owners. Third-party content is reused under, and governed by, its own license terms. The license chosen for the Talenta-specific parts of this release does not apply to third-party content and does not change or replace those terms.

- **Attribution.** Copyright notices, attribution statements and license references contained in third-party content are kept unchanged. Anyone who reuses or redistributes this release must comply with the license terms of each third-party component, including its attribution requirements.
- **No endorsement.** Naming a third party, its vocabulary or its trademark does not imply that the third party endorses, sponsors or is affiliated with the Talenta project or its partners.
- **Trademarks.** All product names, company names and trademarks mentioned are the property of their respective owners and are used for identification only.
- **No warranty.** Third-party content is provided as made available by its owners, without any warranty from the Talenta partners. The Talenta partners accept no liability for the accuracy, completeness or licensing status of third-party content.
- **Corrections.** If you are a rights holder and believe that your work is not correctly attributed or licensed in this release, please contact info@vectorsoft.de. We will correct the attribution or remove the content.

### Allgemeiner Hinweis zu Inhalten Dritter (DE)

Diese Veröffentlichung enthält Vokabulare, Ontologien, Datenmodelle und andere Materialien Dritter („Inhalte Dritter“) oder verweist auf sie; sie sind unten aufgeführt. Alle Rechte an Inhalten Dritter, einschließlich Urheber-, Datenbank- und Markenrechten, verbleiben bei den jeweiligen Rechteinhabern. Inhalte Dritter werden nach den für sie geltenden Lizenzbedingungen nachgenutzt. Die für die Talenta-spezifischen Bestandteile gewählte Lizenz gilt nicht für Inhalte Dritter und ändert oder ersetzt deren Lizenzbedingungen nicht.

- **Namensnennung.** In Inhalten Dritter enthaltene Urheberrechtsvermerke, Namensnennungen und Lizenzhinweise bleiben unverändert erhalten. Wer diese Veröffentlichung nachnutzt oder weitergibt, muss die Lizenzbedingungen jedes Drittbestandteils einhalten, einschließlich der Pflicht zur Namensnennung.
- **Keine Billigung.** Die Nennung eines Dritten, seines Vokabulars oder seiner Marke bedeutet nicht, dass dieser das Projekt Talenta oder seine Partner unterstützt, fördert oder mit ihnen verbunden ist.
- **Marken.** Alle genannten Produkt- und Firmennamen sowie Marken sind Eigentum ihrer jeweiligen Inhaber und werden nur zur Kennzeichnung verwendet.
- **Keine Gewähr.** Inhalte Dritter werden so bereitgestellt, wie sie von ihren Rechteinhabern zur Verfügung gestellt wurden. Die Talenta-Partner übernehmen dafür keine Gewähr und keine Haftung für Richtigkeit, Vollständigkeit oder Lizenzstatus.
- **Korrekturen.** Rechteinhaber, deren Werk nach ihrer Auffassung nicht korrekt genannt oder lizenziert ist, wenden sich bitte an [[KLÄREN: Funktionspostfach]]. Wir korrigieren die Namensnennung oder entfernen den Inhalt.

## Third-party vocabularies included

| Vocabulary (namespace) | Origin | Typed resources in file | Source license (to verify) |
|---|---|---|---|
| iCity ontologies: TransportationSystem, Vehicle, OM, Change, Mereology, SpatialLoc, Time, SSN (`http://ontology.eil.utoronto.ca/icity/…`) | University of Toronto, Enterprise Integration Lab (M. S. Fox, M. Katsumi) | 176 | The header contains `cc:license` CC BY 3.0 |
| ISO 21972 upper-level ontology for smart city indicators, GCI Foundation, GovStat, ISO 5087 generic properties (`http://ontology.eil.utoronto.ca/ISO21972/…`, `…/GCI/…`, `https://standards.iso.org/iso-iec/5087/…`) | University of Toronto EIL; ISO | 159 | to verify (ISO material) |
| WISIB bridge ontologies: Bridge Ontology, Bridge Components, Bridge Structure, Building Material (`https://wisib.de/ontologie/bridge#`, `brcomp#`, `brstr#`, `bmat#`, `brot#`) and example bridge individuals (`https://wisib.de/ontologie/abox/germanroadbridge/d1#`) | WISIB project (creators in the file: Al-Hakam Hamdan, Taras Kozak, Mushtak K. Seeaed) | 230 | The header contains `dc:license` CC BY 1.0 |
| SOSA / SSN (`http://www.w3.org/ns/sosa/`, `http://www.w3.org/ns/ssn/`) | W3C / OGC Spatial Data on the Web WG | 59 | W3C Software and Document License; "Copyright 2017 W3C/OGC" |
| OWL-Time (`http://www.w3.org/2006/time#`) | W3C / OGC | 95 | W3C Software and Document License (to verify) |
| GeoSPARQL (`http://www.opengis.net/ont/geosparql#`) | Open Geospatial Consortium | 42 | OGC Software License |
| GTFS vocabulary (`http://vocab.gtfs.org/terms#`) | Linked GTFS community vocabulary | 99 | to verify (the header contains CC BY 4.0, assignment unclear) |
| Units of Measure OM 1.8 (`http://www.wurvoc.org/vocabularies/om-1.8/`) | Wageningen UR (Rijgersberg et al.) | 28 | to verify |
| IFC (`http://standards.buildingsmart.org/IFCR#`) | buildingSMART | 3 | to verify |
| schema.org, FOAF, SKOS, DCAT, ADMS, BIBO, Dublin Core, VANN, DBpedia ontology | various | annotations and few classes | open licenses (schema.org CC BY-SA 3.0; others to verify) |
