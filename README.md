# Ontology
Ontology of the [MiMoText project](https://mimotext.uni-trier.de/en).

## Context & scope
The MiMoText ontology is dedicated to the domain of literary history and historiography – a broad and far-reaching field of knowledge which we do not intend to address in its entirety. The scope and coverage of the ontology result from the practical requirements of the realization of our knowledge graph and the associated concerns.
An essential particularity of our domain is that we model perspectives rather than facts. Therefore, the possibilities of the linked open data paradigm to let complementary and also contradictory statements coexist are very useful to us. This particularity has the consequence that 'reification' (i.e., statements about statements) is an important modeling dimension that includes, among other things, the unambiguous referencing of each statement, including linkage to the dataset to which it can be traced.

*Reference publication:*
Schöch, Christof, Maria Hinzmann, Röttgermann Julia, Anne Klee, and Katharina Dietz. “Smart Modelling for Literary History.” IJHAC: International Journal of Humanities and Arts Computing [Special Issue on Linked Open Data] 16, no. 1 (2022): 78–93. (https://doi.org/10.3366/ijhac.2022.0278).

## Aims
1. One goal of the ontology is to structure data in the project "Mining and Modeling Text". Essentially, this project is about extracting heterogeneous data from three different types of sources using quantitative methods (mining) and linking them in such a way (modeling) that they can be aggregated in a queryable knowledge graph and offer interesting perspectives as well as innovative research opportunities for researchers.
2. We consider the French Enlightenment novel as an example and designed our project and the ontology to be transferable to other domains of the humanities (philosophy, history and cultural studies, art history, etc.).

## Structure
We structure the ontology in modules to increase interoperability, reuse possibilities, and reproducibility. The objectives can be differentiated:

* Clarity & reproducibility: The conceptual decisions as well as our source data are thereby understandable and traceable in individual 'packages'.
* Transferability: Some challenges are also relevant in other Computational Literary Studies projects as well as in Digital Humanities in general, especially in the linked open data context.
* Use of MiMoTextBase via the SPARQL-endpoint: In particular, more complex queries require a thorough knowledge of the data model and the imported data. In addition to our tutorial, the ontology should enable the formulation of SPARQL-queries (especially for those who already have SPARQL knowledge) and an interest-specific, targeted understanding of the data model.

## Modules
The modules are heterogeneous in scope respectively coverage. Within the modules, all essential modeling decisions are represented and reflected.
The functionality of Wikibase as well as conventions and standards in Wikidata are crucial for our modeling decisions. We have taken other standards into account where possible and will expand this in the future (see below).
There are currently 8 completed modules, and another 3 in progress or planned:

* Module 1: thematic statement
* Module 2: spatial statement
* Module 3: narrative form
* Module 4: literary work
* Module 5: author
* Module 6: mapping [under construction]
* Module 7: referencing
* Module 8: versioning & publication
* Module 9: terminology
* Module 10: bibliography [under construction]
* Module 11: scholarly work [planned]

These modules are related to and based on two pilot projects (1 & 2), a statement type that is central to our domain (3), our two central entity types or 'classes' (4 and 5), three further modules that represent central challenges and our approaches to solving them (6-7), as well as one for integrating the different source types including data sets (8) and a module that represents the modeling of our multilingual controlled vocabularies and depicts terminological decisions (9).
Furthermore, two further modules are planned that address more detailed the different source types of MiMoText: a module on our main bibliographic source (10) and a module for the scholarly literature data (11). In the visualizations of the ontology version 1.0, in all modules the Q-items and properties are represented for which data are already available in the MiMoTextBase. In some cases we have highlighted extension plans for the near future in gray.

**[Module overview and visualizations](https://github.com/MiMoText/ontology/blob/main/Modules%20overview.md)**

The visualizations were created using the software [VUE (= Visual Understanding Environment)](https://vue.tufts.edu/), an open source project of Tufts University.

## Formal representation and reuse
This repository addresses so far mainly the conceptual representation. The ontology is part of the MiMoTextBase and downloadable as an RDFdump for further use in a local Wikibase.
We are thinking about making the overall ontology as well as the individual modules available as OWL files, also depending on feedback about possible usage scenarios. Flexible visualization of the ontology would be one of the benefits.

## Modeling approach & decisions
We are not attempting to model the entire domain of literary history and historiography deductively, but rather based on our purpose to connect inductively the different data source types.
Where possible and necessary, for example in the case of the narrative form, we have conceptually addressed the corresponding theoretical concepts and strived for a mediation that increases plausibility and acceptance among literary scholars. Each module, which has only been visualized so far, is explained and more detail in the various decisions made in the modeling process.
We are planning further steps (see below).

## Infrastructure & prefixes

### Open Science
For the provision of data, we follow open science principles, such as the publication of FAIR data in open access as well as the use of open source software – in particular Wikibase. We created a [custom bot using the Python library Pywikibot](https://github.com/MiMoText/Wikibase-Bot) to import and update the RDF triples into our Wikibase instance from TSV files.

### Wikibase ecosystem
We understand our [MiMoTextBase](https://docs.mimotext.uni-trier.de) as part of the Wikibase ecosystem with the decision for a local Wikibase instance. The infrastructure of a local Wikibase has a significant influence on the data model and therefore also on the query possibilities.

### Prefixes (status quo)
Currently we still have the Wikibase "default settings", so we have exactly the prefixes for our MiMoTextBase that Wikidata uses. We have defined these for our MiMoTextBase, i.e. a local Wikibase instance, as follows:

- prefix wd: http://data.mimotext.uni-trier.de/entity/
- prefix wdt: http://data.mimotext.uni-trier.de/prop/direct/
- prefix ps: http://data.mimotext.uni-trier.de/prop/statement/
- prefix pr: http://data.mimotext.uni-trier.de/prop/reference/
- prefix p: http://data.mimotext.uni-trier.de/prop

For further prefixes and a visualization of the Wikidata / Wikibase data model see: https://en.wikibooks.org/wiki/SPARQL/WIKIDATA_Qualifiers,_References_and_Ranks#/media/File:SPARQL_data_representation.png

## Future work
### Prefixes (future plans)
Regarding the prefixes, we have decided to change in the near future the prefixes currently available in our local Wikibase, which correspond to those of Wikidata, so that, among other things, no confusion arises with 'federated queries'. We will stay within the Wikidata logic of the labeling to increase usability for those who are already familiar with the Wikidata prefixes (e.g. 'mmd' for the 'entities' with the prefix 'wd', 'mmdt' for the 'properties' instead of 'wdt').

### Linking with the Wikidata-Graph
In the context of linking to the Wikidata cloud, we currently have several phases planned in the spirit of the 'Wikibase ecosystem', although we will probably not be able to realize all of them in the current project phase:
* mapping of thematic and spatial concepts in our controlled vocabularies (done).
* mapping of properties and classes (done)
* mapping of author and work items (in progress)
* creation of a MiMoText ID in Wikidata (future)
* linking the literary works we could map from Wikidata to the work items in our MiMoTextBase (future)
* importing the work items not yet available in Wikidata into Wikidata and also linking them to our MiMoTextBase. (future)

An interesting model project for this approach is the [WeChangEd project](https://www.wechanged.ugent.be/). Beyond that we would also be happy to have the opportunity to link our data in the sense of Linked Open Data to further ressources.For some authority data we have already considered this (VIAF, GND e.g.)

### Further interoperability & reuse
We plan to further increase interoperability by a formal representation for different user groups: a) For users within the wikiverse, this will be done via 'entity schemes'. b) In the spirit of the general W3C standard, this will involve a representation of the ontology in OWL created with the ontology editor [Protégé](https://protege.stanford.edu/).
With regard to reuse and mapping, we have so far focused on Wikidata, which we see as a kind of 'hub'. In the development of the ontology, we have explored other projects in or neighboring our domain and tried to integrate solution approaches, if they were transferable, into our modeling (e.g. [ArtBase](https://artbase.rhizome.org/wiki/Main_Page), [ONAMA](http://onama.sbg.ac.at), [Enslaved.org](https://enslaved.org/), [Krater/O4DH](http://o4dh.com/datasets). The [ELTeC project](https://www.distant-reading.net/eltec/) is particularly related, insofar as it also involves modeling novel data in Wikidata (Nešić et al. 2021). However, while in European Literary Text Collection (ELTeC) the differentiation between the literary work and different edition versions is very important, we have decided to put the literary work in the center and to avoid further differentiations within our MiMoTextBase in order to reduce complexity.

### Documentation and formalization in other standards
We will provide a more detailed documentation considering our modeling decisions.
The formal representation and documentation of the modeling decisions will be gradually added to this repository as well as to our MiMoTextBase. We are also aiming for a representation in OWL.
The field of validation (e.g. via SHACL, ShEx) should be thought through and expanded.
We plan to represent all classes (Q-items) and properties in their module structure, so that they and their associated instance data can be easily retrieved via SPARQL-query.

### Reification & inference
We have so far focused mainly on referencing (see referencing module) and conceptualized to use simple qualifiers (e.g. counting text occurrences with the property "occurence in text"). We have not yet made use of all the potential of the Wikibase infrastructure, for example, for ranking statements or modeling different reliabilities of statements. However, we have discussed this in the context of ranking topics for more precise modeling of thematic statements based on topic modeling.
The question of inferring statements from other statements (implicit statements) is different within the data model of Wikibase (and our ontology working with it) than in ontologies that follow the OWL standards more strictly and in particular make a clear separation of classes and instance data ('individuals'). This separation does not exist in the Wikibase ecosystem, which has consequences for inferences. Nevertheless, inference is of course possible, also insofar as there are efforts to increase the interoperability of the Wikibase data model.

### Further information
See also: [About MiMoTextBase](https://mimotext.github.io/MiMoTextBase_Tutorial/aboutMiMoTextBase.html)

## Community
An ontology is not an ontology as long as it is only used in one project. We therefore see it rather as an ontology proposal. We would like to discuss our modeling decisions in exchange with colleagues from Computational Literary Studies as well as other fields of Digital Humanities in order to jointly develop the ontology for the community, i.e. a data model that can structure information in different projects and link them in the spirit of Linked Open Data.
We would also like to get in closer contact with literary scholars to extend the modeling of the relevant types of statements we have identified.

## Bibliography
* Arenas, Marcelo, Claudio Gutierrez, and Jorge Pérez. 2010. “On the Semantics of SPARQL.” In Semantic Web Information Management: A Model-Based Perspective, edited by Roberto de Virgilio, Fausto Giunchiglia, and Letizia Tanca, 281–307. Berlin, Heidelberg: Springer. https://doi.org/10.1007/978-3-642-04329-1_13.
* Eells, Andrew, Cogan Shimizu, Lu Zhou, Pascal Hitzler, and Dean Rehberger. 2021. “Aligning Patterns to the Wikibase Model.” In Http://Ontologydesignpatterns.Org/Wiki/WOP:2021. https://daselab.cs.ksu.edu/sites/default/files/WOP2021_paper_4.pdf.
* Gangemi, Aldo, and Valentina Presutti. 2009. “Ontology Design Patterns.” In Handbook on Ontologies, 221–43. https://doi.org/10.1007/978-3-540-92673-3_10.
* Gruber, Thomas R. 1995. “Toward Principles for the Design of Ontologies Used for Knowledge Sharing?” International Journal of Human-Computer Studies 43 (5): 907–28. https://doi.org/10.1006/ijhc.1995.1081.
* Hitzler, P. 2021. “A Review of the Semantic Web Field.” Commun. ACM. https://doi.org/10.1145/3397512.
* Hitzler, P., M. Krötzsch, and S. Rudolph. 2009. “Foundations of Semantic Web Technologies.” In . https://doi.org/10.1201/9781420090512.
* Hitzler, Pascal, Aldo Gangemi, Krzysztof Janowicz, Adila Krisnadhi, and Valentina Presutti, eds. 2016. Ontology Engineering with Ontology Design Patterns: Foundations and Applications. Studies on the Semantic Web, vol. 025. Berlin, Germany : Amsterdam, Netherlands: Akademische Verlagsgesellschaft ; IOS Press.
* Ikonić Nešić, Milica, Ranka Stanković, and Biljana Rujević. 2021. “Serbian ELTeC Sub-Collection in Wikidata.” Infotheca 21 (2): 60–86. https://doi.org/10.18485/infotheca.2021.21.2.4.
* Janowicz, Krzysztof, Aldo Gangemi, Pascal Hitzler, Adila Krisnadhi, and Valentina Presutti. 2016. “Introduction: Ontology Design Patterns in a Nutshell.” In Ontology Engineering with Ontology Design Patterns: Foundations and Applications, edited by Pascal Hitzler, Aldo Gangemi, Krzysztof Janowicz, Adila Krisnadhi, and Valentina Presutti. Studies on the Semantic Web, vol. 025. Berlin, Germany : Amsterdam, Netherlands: Akademische Verlagsgesellschaft ; IOS Press. https://people.cs.ksu.edu/~hitzler/pub2/00-introduction.pdf.
* Noy, Natalya F., and Deborah L. McGuinness. 2001. “Ontology Development 101: A Guide to Creating Your First Ontology.” https://protege.stanford.edu/publications/ontology_development/ontology101.pdf.
* Rehbein, Malte. 2017. “Ontologien.” In Digital Humanities, edited by Fotis Jannidis, Hubertus Kohle, and Malte Rehbein, 162–76. Stuttgart: Metzler. https://doi.org/10.1007/978-3-476-05446-3_11.
* Röttgermann, Julia, and Christof Schöch. 2020. “FAIRe Daten in Den Literaturwissenschaften? Das Beispiel „Mining and Modeling Text“ Und Der Französische Roman Des 18. Jahrhunderts.” Romanistik-Blog. Blog Des Fachinformationsdienstes (blog). 2020. https://blog.fid-romanistik.de/2020/11/05/faire-daten-in-den-literaturwissenschaften/.
* Shimizu, Cogan, Karl Hammar, and Pascal Hitzler. 2021. “Modular Ontology Modeling.” Semantic Web – Interoperability, Usability, Applicability. http://www.semantic-web-journal.net/content/modular-ontology-modeling-1.
* Shimizu, Cogan, Quinn Hirt, and Pascal Hitzler. 2019. “MODL: A Modular Ontology Design Library.” ArXiv:1904.05405 [Cs], April. http://arxiv.org/abs/1904.05405.
