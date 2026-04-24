# EKC Data Model Ontology in OWL/Turtle

EKC Data Model Ontology is a domain-specific vocabulary for modeling entities and relationships in Korean cultural heritage, especially historical facts, source documents, persons, places, institutions, and related knowledge structures.

It has been developed at [**the Center for Digital Humanities, the Academy of Korean Studies (AKS)**](https://dh.aks.ac.kr/) since 2016, initially for the digitization of the *Encyclopedic Archives of Korean Culture*, and has been further refined through subsequent digital humanities projects and researches at the Center. [**EKC Data Model Ontology in OWL/Turtle**](https://doi.org/10.5281/zenodo.19059550) builds on the earlier wiki-based [*Ontology:EKC 2022*](https://dh.aks.ac.kr/~hanyang2/wiki/index.php/Ontology:EKC_2022) and rearticulates it as a citable OWL/Turtle ontology repository.

The present release line strengthens versioning, publication metadata, and repository-level documentation so that the ontology can be maintained, cited, and reused in a more stable and standards-aware form. Since **v2025.1.17**, the repository also makes a clearer distinction between the **core EKC ontology line** and derivative/project-local extension logic that may be maintained outside the core TTL.

*EKC(Encyves of Korean Culture) 데이터 모델 온톨로지*는 한국의 전통문화 속의 역사적 사실 관계 및 그 사실의 문헌적 근거에 관한 지식을 데이터화 하기 위해 개발한 온톨로지 스키마입니다. (*Encyves* ≒ *Encyclopedic Archives*) 이 모델은 [**한국학중앙연구원 디지털인문학연구소**](https://dh.aks.ac.kr/)에서 2016년에 처음 제정하였고([EKC 1.0/2016, EKC 1.1/2027](http://dh.aks.ac.kr/Encyves/wiki/index.php/EKC_Data_Model-Draft_1.1)), 매년 유관 분야 연구를 통해 확장해 가고 있습니다.

[**EKC Data Model Ontology in OWL/Turtle**](https://doi.org/10.5281/zenodo.19059550) 저장소는 기존의 위키 기반 [*Ontology:EKC 2022*](https://dh.aks.ac.kr/~hanyang2/wiki/index.php/Ontology:EKC_2022)를 OWL/Protégé 및 Turtle 기반의 인용 가능한 온톨로지 릴리즈로 정식화한 것이며, 버전 관리, 출판 메타데이터, 시맨틱웹 표준 적합성, 저장소 문서화 측면에서 추가적인 개선을 반영합니다. 특히 **v2025.1.17**부터는 EKC 본체(core line)와 파생·로컬 확장 계열의 역할 구분을 더 명확히 하였습니다.

## Quick Facts

- **Namespace:** `http://dh.aks.ac.kr/ontologies/ekc#`
- **Prefix:** `ekc`
- **Format:** Turtle (`.ttl`), OWL 2
- **License:** CC BY-SA 4.0
- *Concept* **DOI (all versions):** `10.5281/zenodo.19059550`
- **Current stable release:** [EKC 2025 [v2025.1.17]](https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.17)
- *Version* **DOI (v2025.1.17):** `TBD at release`

## Overview

The EKC Data Model Ontology provides a structured semantic framework for representing Korean traditional culture and related historical knowledge.

It is intended for ontology-based knowledge organization, linked data production, and humanities data modeling. The present repository provides the ontology in OWL using Protégé and in Turtle serialization for publication, maintenance, and reuse.

## Latest Stable Release

### EKC 2025 [v2025.1.17]

- **Release page:** <https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.17>
- **Status:** Current stable release
- *Version* **DOI (v2025.1.17):** `TBD at release`
- *Concept* **DOI (all versions):** `10.5281/zenodo.19059550` [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19059550.svg)](https://doi.org/10.5281/zenodo.19059550)

## Archived Versions

- **Note:** Preserved for reproducibility, legacy dataset compatibility, and stable scholarly citation

### EKC 2025 [v2025.1.0]
- **Release page:** <https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.0>
- **Status:** Archived

### EKC 2025 [v2025.0.0]
- **Release page:** <https://github.com/dongshins/EKC_ontology/releases/tag/v2025.0.0>
- **Status:** Archived

### EKC 2022.α2507 [v2022-alpha2507]
- **Release page:** <https://github.com/dongshins/EKC_ontology/releases/tag/v2022-alpha2507>
- **Status:** Archived

## Key Classes

- `ekc:Actor`
- `ekc:Event`
- `ekc:Place`
- `ekc:Architecture`
- `ekc:Clothing`
- `ekc:Food`
- `ekc:Object`
- `ekc:Work`
- `ekc:Record`
- `ekc:Concept`
- `ekc:Heritage`
- `ekc:Multimedia`
- `ekc:WebResource`
- `ekc:Bibliography`
- `ekc:Text`
- `ekc:Story`
- `ekc:Index`

## Technical Notes

- **Version history:** EKC 1.0 → EKC 1.1 → EKC 2022 → EKC 2022.α2507 → EKC 2025 [v2025.0.0] → EKC 2025 [v2025.1.0] → EKC 2025 [v2025.1.17]
- **Primary ontology file:** [ekc_ontology.ttl](./ekc_ontology.ttl)
- **Version archive:** [version_history/](./version_history)

### Core / derivative scope note (v2025.1.17) / 본체·파생 범위 구분 부기(附記)

- The EKC repository is maintained as the **core ontology line** for the EKC namespace and release series.
- Since `v2025.1.17`, the published EKC TTL intentionally carries a slimmer local overlay for identity/mapping policy than `v2025.1.0`.
- Ontology-header `dcterms:issued` / `dcterms:modified` values are now serialized as `xsd:date`, and their annotation-property ranges are relaxed to `rdfs:Literal`.
- `owl:sameAs` remains available in EKC, but its local descriptive block was simplified and its earlier transitive typing was removed.
- Local EKC-side redeclarations for `skos:mappingRelation`, `skos:exactMatch`, and `skos:closeMatch` were removed from the published TTL.
- Derivative or project-local extension logic—such as stronger local mapping guidance or date-oriented extension policy—may be maintained in a separate derivative ontology line rather than in the EKC core TTL itself.
- See details in: [docs/changes/v2025.1.17-ontology-revision.md](./docs/changes/v2025.1.17-ontology-revision.md)

### Standards & Reference Models (Addendum) / 표준·참조모델 부기(附記)

CIDOC CRM (ISO 21127:2023; corresponds to CIDOC CRM community version 7.1.3) and CBDB were consulted as conceptual references during early EKC modeling.

However, due to the project’s namespace policy, readability considerations, and internal terminology system, this repository does **not** import CIDOC CRM and CBDB nor directly reuse the `crm:`, `cbdb:`, `shlib:` prefixes.

Unless explicitly stated, such references are conceptual only and do **not** imply formal compliance or full alignment.

## Links

- **Ontology file:** [ekc_ontology.ttl](./ekc_ontology.ttl)
- **Version history:** [version_history/](./version_history)
- **Detailed revision note:** [docs/changes/v2025.1.17-ontology-revision.md](./docs/changes/v2025.1.17-ontology-revision.md)
- **Derivative extension line (EKCD):** <https://github.com/dongshins/ekcd-ontology>
- **LOV registration:** [EKC Data Model Vocabulary: Ontology Design for the Encyclopedic Archives of Korean Culture (ekc)](https://lov.linkeddata.es/dataset/lov/vocabs/ekc)

## Credits

The EKC Ontology was initially developed through **collaborative work** at **the Academy of Korean Studies** under the guidance of [**Professor Hyeon KIM (김현 @ko)**](http://www.xuanflute.com/).

For the **full contributor list and roles**, see [**CONTRIBUTORS.md**](./CONTRIBUTORS.md). The OWL/Protégé-based version of the ontology in this repository, together with Turtle serialization and repository maintenance, has been composed and maintained by **Dong Shin SEO**.

## Related Notes

- [Ontology:EKC 2022](https://dh.aks.ac.kr/~hanyang2/wiki/index.php/Ontology:EKC_2022)
- [Protégé](https://protege.stanford.edu)
- [Turtle Draft for EKC Data Model](https://dh.aks.ac.kr/~dongshin/wiki/index.php/Turtle_Draft_for_EKC_Data_Model)

## License

Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
