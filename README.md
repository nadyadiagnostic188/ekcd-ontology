# EKCD

EKCD is an EKC-derived ontology in OWL/Turtle designed to refine and extend selected areas of the EKC data model for more explicit, maintainable, and reusable knowledge modeling. Developed by Dong Shin SEO, it preserves conceptual continuity with EKC while supporting further specialization for Korean cultural heritage and digital humanities research.

**Repository:** `ekcd-ontology`  
**Ontology title:** `EKCD: EKC Derived Ontology`  
**Namespace prefix:** `ekcd:`  
**Preferred namespace URI:** `http://dh.aks.ac.kr/ontologies/ekcd#`

---

## Overview

EKCD is a derivative ontology based on the previously released EKC ontology.  
It is designed to support ongoing personal extensions, especially in areas that were not formally incorporated into the institutional EKC release line.

Rather than replacing EKC, EKCD is intended as:

- a **derived ontology** that preserves conceptual continuity with EKC,
- a **working extension layer** for newly introduced properties and modeling decisions,
- a **practical ontology base** for building ABox and links datasets through Protégé and Cellfie.

---

## Relationship to EKC

EKCD is derived from EKC and is intended to remain interoperable with it.

In principle:

- **institutional EKC** remains the public institutional baseline,
- **EKCD** manages selected personal extensions and refinements by Dong Shin SEO,
- datasets built in the current workflow may use **EKCD as the active TBox** while still reusing the conceptual backbone of EKC.

EKCD therefore should be understood as a **derivative and extensible companion ontology**, not as a direct replacement for EKC.

---

## Scope of EKCD

At the current stage, EKCD is intended to host:

1. additional datatype properties needed for ongoing dataset construction, including:
   - `ekcd:occurrenceDate`
   - `ekcd:startDate`
   - `ekcd:endDate`
   - `ekcd:originalDate`
   - `ekcd:accessURL`

2. operational annotation guidance for external mapping practice involving standard properties such as:
   - `owl:sameAs`
   - `skos:exactMatch`
   - `skos:closeMatch`
   - `skos:mappingRelation`

3. ontology maintenance and extension work conducted personally by Dong Shin SEO outside the institutional EKC release line

---

## Design Principles

EKCD follows these practical principles:

- **continuity with EKC** wherever possible
- **clear separation** between institutional and personal release lines
- **reuse of standard vocabularies** instead of minting unnecessary local equivalents
- **compatibility with spreadsheet-based data production**, especially through Protégé + Cellfie workflows
- **separation of ABox data and external links datasets** for cleaner maintenance

---

## Namespace and Versioning

- **Ontology IRI:** `http://dh.aks.ac.kr/ontologies/ekcd`
- **Namespace URI:** `http://dh.aks.ac.kr/ontologies/ekcd#`
- **Prefix:** `ekcd:`
- **Version example:** `EKCD v0.9.7`

Versioned snapshots may be stored separately from the working ontology file for stable citation and release management.

---

## Repository Structure

```text
ekcd-ontology/
├─ README.md
├─ CHANGELOG.md
├─ LICENSE
├─ .zenodo.json
├─ /vocab/
│  ├─ ekcd.ttl
│  ├─ versions/
│  │  └─ ekcd_v1_2_3.ttl
│  └─ snapshots/
│     └─ ekcd_2026-04-05_1.ttl
├─ /docs/
│  ├─ releases/
│  │  └─ v1.2.3.md
│  └─ changes/
│     └─ v1.2.3-ontology-revision.md
├─ /templates/
│  └─ EKCD_Cellfie_Template.xlsx
└─ /checksums/
   └─ sha256.txt
```
---

## Data Production Workflow

EKCD is intended to support a practical workflow such as:
- maintain the TBox in **Protégé**
- prepare researcher input in spreadsheet templates
- transform spreadsheet data into RDF/OWL through **Cellfie**
- generate:
  - an **ABox dataset**
  - a separate **links dataset**
- validate and review outputs before public release

This repository is therefore not only an ontology publication space, but also a maintenance base for ontology-driven dataset production.

---

## Citation

A Zenodo DOI will be used for formal citation once the corresponding GitHub release is archived.

Suggested citation form will be added after the first DOI-backed release.

---

## Maintainer

**Dong Shin SEO**

EKCD is maintained as a personal derivative ontology line based on EKC, for ongoing ontology refinement and dataset construction in Korean cultural heritage and digital humanities contexts.

---

## License

Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
