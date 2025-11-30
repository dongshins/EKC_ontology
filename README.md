# Ontology using Protégé : EKC Data Model 

The EKC Ontology is a domain-specific vocabulary for encoding relationships among historical facts, sources, persons, and works in traditional Korean culture. 

Developed since 2016 under the Center for Digital Humanities in the Academy of Korean Studies.

Namespace: `http://dh.aks.ac.kr/ontologies/ekc#`

Prefix: `ekc`

License: CC BY-SA 4.0

Current version: v2022.α2507 (2025 update)

EKC(Encyves of Korean Culture) 데이터 모델은 한국의 전통문화 속의 역사적 사실 관계 및 그 사실의 문헌적 근거에 관한 지식을 데이터화 하기 위해 개발한 온톨로지 스키마입니다.(Encyves ≒ Encyclopedic Archives) 한국학중앙연구원 디지털인문학연구소에서 2016년에 처음 제정하였고([EKC 1.0/2016, EKC 1.1/2027](http://dh.aks.ac.kr/Encyves/wiki/index.php/EKC_Data_Model-Draft_1.1)), 매년 유관 분야 연구를 통해 확장해 가고 있습니다.

The present specification is based on the document "[Ontology:EKC 2022](https://dh.aks.ac.kr/~hanyang2/wiki/index.php/Ontology:EKC_2022)", originally led by **Hyeon KIM (Professor, AKS)** in the Center for Digital Humanities at the Academy of Korean Studies.

## Key Classes

- `ekc:Actor`: Historical figures; Organizations as collective actors and institutions as operating entities  
- `ekc:Event`: Events held in a certain area, ceremonies and events that reproduce them today  
- `ekc:Place`: Places related to historical events or characters; Places where historical relics or artifacts are located  
- `ekc:Architecture`: Historic Buildings in a certain area and historically related structures  
- `ekc:Clothing`: Costumes, components of costumes, or traditional ornaments  
- `ekc:Food`: Food, ingredients and table setting  
- `ekc:Object`: Items used in various ceremonies or events; Items or tools that show the culture of the time  
- `ekc:Work`: Works of art such as literature, fine arts, music, dance, performance, etc.  
- `ekc:Record`: Records that serve as the source of knowledge such as books, photographs, drawings, and inscriptions  
- `ekc:Concept`: Terms and concepts necessary to explain institutions, rituals, customs, etc.  
- `ekc:Heritage`: Registration information of designated and registered cultural properties  
- `ekc:Multimedia`: 3D model of a building; 3D map indicating the location of a specific place; visual materials  
- `ekc:WebResource`: Reference materials that can be accessed on the World Wide Web  
- `ekc:Bibliography`: List of academic research materials  
- `ekc:Text`: Text in the literature that functions as evidence of explanation  
- `ekc:Story`: Description of historical knowledge that explains the background of discovering data nodes  
- `ekc:Index`: A list of nodes of similar character. Timeline, collection list, reference list, web resource list, etc.  

## Technical Details

- Format: Turtle (.ttl), OWL 2
- Accessible at: raw URL
- Version history: EKC 1.0 → EKC 1.1 → EKC 2022 → EKC 2022.α2507
- License: Creative Commons Attribution‑ShareAlike 4.0 International (CC BY‑SA 4.0)

## Links

- Ontology file: [ekc_ontology.ttl](./ekc_ontology.ttl)  
- Version history: [version_history/](./version_history)  
- Publication: [EKC Data Model Vocabulary: Ontology Design for the Encyclopedic Archives of Korean Culture (ekc)](https://lov.linkeddata.es/dataset/lov/vocabs/ekc)(LOV registration)

## Contributors

The EKC Ontology was initially developed during collaborative efforts at the Academy of Korean Studies, under the guidance of **Professor Hyeon KIM**. The early modeling team included over ten researchers who contributed to the conceptual framework and design.

Since its inception, the ontology has been improved and maintained through various projects in the field of digital humanities.

The version of the ontology created in OWL using Protégé and serialized in Turtle format was solely authored and structured by:

**Dong Shin SEO**  
Researcher, Center for Digital Humanities, Academy of Korean Studies  
IT Expert Adviser, Division of Information Development, Academy of Korean Studies  
Email: oriental.neo@gmail.com


※ [Protégé](https://protege.stanford.edu) : Developed by the Stanford Center for Biomedical Informatics Research at the Stanford University School of Medicine.

※ [Turtle draft for EKC Data Model](https://dh.aks.ac.kr/~dongshin/wiki/index.php/Turtle_Draft_for_EKC_Data_Model) : Wiki page since 2024-09-23 by Dong Shin SEO 

※ [EKC ontology using Protégé](https://github.com/dongshins/EKC_ontology) (this repository) : Since 2024-09-28 by Dong Shin SEO 

※ Advanced EKC ontology using Protégé : Separated as 'EKC_ontology_advanced' repository since 2024-11-23 by Dong Shin SEO 

# License for this repository 
Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg

※ [Creative Commons Licenses for GitHub Projects](https://github.com/santisoler/cc-licenses) : Easy ways for applying Creative Commons Licenses on Github repositories through Markdown language by [Santiago Soler and contributors](https://github.com/santisoler/cc-licenses) 
