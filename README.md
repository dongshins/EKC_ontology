# EKC Data Model Ontology

EKC Data Model Ontology is a domain-specific vocabulary for modeling entities and relationships in Korean cultural heritage, especially historical facts, source documents, persons, places, institutions, and related knowledge structures.

It has been developed at [**the Center for Digital Humanities, the Academy of Korean Studies (AKS)**](https://dh.aks.ac.kr/) since 2016—initially for the digitization of the *Encyclopedic Archives of Korean Culture*—and has been further refined through subsequent digital humanities projects and researches at the Center.

*EKC(Encyves of Korean Culture)* 데이터 모델은 한국의 전통문화 속의 역사적 사실 관계 및 그 사실의 문헌적 근거에 관한 지식을 데이터화 하기 위해 개발한 온톨로지 스키마입니다.(Encyves ≒ Encyclopedic Archives) [**한국학중앙연구원 디지털인문학연구소**](https://dh.aks.ac.kr/)에서 2016년에 처음 제정하였고([EKC 1.0/2016, EKC 1.1/2027](http://dh.aks.ac.kr/Encyves/wiki/index.php/EKC_Data_Model-Draft_1.1)), 매년 유관 분야 연구를 통해 확장해 가고 있습니다. @ko

## Quick Facts

- **Namespace:** `http://dh.aks.ac.kr/ontologies/ekc#`
- **Prefix:** `ekc`
- **Format:** Turtle (`.ttl`), OWL 2
- **License:** CC BY-SA 4.0
- **Current stable release:** [EKC 2025 [v2025.1.0]](https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.0)

## Overview

The EKC Data Model Ontology provides a structured semantic framework for representing Korean traditional culture and related historical knowledge. It is intended for ontology-based knowledge organization, linked data production, and humanities data modeling.

The present repository provides the ontology in OWL using Protégé and in Turtle serialization for publication, maintenance, and reuse.

## Latest Stable Release

### EKC 2025 [v2025.1.0]

- **Release page:** <https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.0>
- **Status:** Current stable release

## Archived Versions
- **Note:** Preserved for reproducibility, legacy dataset compatibility, and stable scholarly citation

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

- **Version history:** EKC 1.0 → EKC 1.1 → EKC 2022 → EKC 2022.α2507 → EKC 2025
- **Primary ontology file:** [ekc_ontology.ttl](./ekc_ontology.ttl)
- **Version archive:** [version_history/](./version_history)

### Standards & Reference Models (Addendum) / 표준·참조모델 부기(附記)

CIDOC CRM was consulted as a conceptual reference during early EKC modeling. However, due to the project’s namespace policy, readability considerations, and internal terminology system, this repository does **not** import CIDOC CRM nor directly reuse the `crm:` prefix.

Unless explicitly stated, such references are conceptual only and do **not** imply formal compliance or full alignment.

## Links

- **Ontology file:** [ekc_ontology.ttl](./ekc_ontology.ttl)
- **Version history:** [version_history/](./version_history)
- **LOV registration:** [EKC Data Model Vocabulary: Ontology Design for the Encyclopedic Archives of Korean Culture (ekc)](https://lov.linkeddata.es/dataset/lov/vocabs/ekc)

## Credits

The EKC Ontology was initially developed through **collaborative work** at **the Academy of Korean Studies** under the guidance of [**Professor Hyeon KIM (김현 @ko)**](http://www.xuanflute.com/).

For the **full contributor list and roles**, see [**CONTRIBUTORS**.md](./CONTRIBUTORS.md).

The OWL/Protégé-based version of the ontology in this repository, together with Turtle serialization and repository maintenance, has been composed and maintained by **Dong Shin SEO**.

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
