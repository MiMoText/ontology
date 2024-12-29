# Ontology
Ontology of the [MiMoText project](https://mimotext.uni-trier.de/en).

## Context & scope
The MiMoText ontology is dedicated to the domain of literary history and historiography – a broad and far-reaching field of knowledge which we do not intend to address in its entirety. The scope and coverage of the ontology result from the practical requirements of the realization of our knowledge graph and the associated concerns.
An essential particularity of our domain is that we model perspectives rather than facts. Therefore, the possibilities of the linked open data paradigm to let complementary and also contradictory statements coexist are very useful to us. This particularity has the consequence that 'reification' (i.e., statements about statements) is an important modeling dimension that includes, among other things, the unambiguous referencing of each statement, including linkage to the dataset to which it can be traced.

*Reference publication:*
* Schöch, Christof, Maria Hinzmann, Julia Röttgermann, Katharina Dietz, and Anne Klee. 2022. “Smart Modelling for Literary History.” International Journal of Humanities and Arts Computing 16 (1): 78–93. https://doi.org/10.3366/ijhac.2022.0278.
* Hinzmann, Maria, Matthias Bremm, Tinghui Duan, Anne Klee, Johanna Konstanciak, Julia Röttgermann, Christof Schöch, and Joëlle Weis. 2024. “Patterns in Modeling and Querying a Knowledge Graph for Literary History (Preprint).” Zenodo. https://doi.org/10.5281/zenodo.12080340.


## Aims
1. One goal of the ontology is to structure data in the project "Mining and Modeling Text". Essentially, this project is about extracting heterogeneous data from three different types of sources using quantitative methods (mining) and linking them in such a way (modeling) that they can be aggregated in a queryable knowledge graph and offer interesting perspectives as well as innovative research opportunities for researchers.
2. We consider the French Enlightenment novel as an example and designed our project and parts of the ontology to be transferable to other domains of the humanities (philosophy, history and cultural studies, art history, etc.).

## Structure
We structure the ontology in modules to increase interoperability, reuse possibilities, and reproducibility. The objectives can be differentiated:

* Clarity & reproducibility: The conceptual decisions as well as our source data are thereby understandable and traceable in individual 'packages'.
* Transferability: Some challenges are also relevant in other Computational Literary Studies projects as well as in Digital Humanities in general, especially in the linked open data context.
* Use of MiMoTextBase via the SPARQL-endpoint: In particular, more complex queries require a thorough knowledge of the data model and the imported data. In addition to our tutorial, the ontology should enable the formulation of SPARQL-queries (especially for those who already have SPARQL knowledge) and an interest-specific, targeted understanding of the data model.

## Modules
The modules are heterogeneous in scope respectively coverage. Within the modules, all essential modeling decisions are represented and reflected.
The functionality of Wikibase as well as conventions and standards in Wikidata are crucial for our modeling decisions. We have taken other standards into account where possible and would like to expand this in the future.
There are currently 13 completed modules:

* Module 1: theme
* Module 2: space
* Module 3: narrative form
* Module 4: literary work
* Module 5: author
* Module 6: mapping
* Module 7: referencing
* Module 8: versioning & publication
* Module 9: terminology
* Module 10: bibliography
* Module 11: scholarly work
* Module 12: literary work analysis
* Module 13: federation

These modules are related to and based on two pilot projects (1 & 2), a statement type that is central to our domain (3), our two central entity types or 'classes' (4 and 5), two further modules that represent central challenges and our approaches to solving them (6-7), as well as one for integrating the different source types including data sets (8) and a module that represents the modeling of our multilingual controlled vocabularies and depicts terminological decisions (9). Two further modules address more detailed the different source types of MiMoText: a module on our main bibliographic source (10) and a module for the scholarly work data (11). Module 12 concerns the analysis of literary works (topic modeling, sentiment analysis, stylometry) and Module 13 represents the modeling decisions around bidirectional federation with Wikidata. 

**[Module overview and visualizations](https://github.com/MiMoText/ontology/blob/main/Modules%20overview.md)**


The visualizations were created using the software [VUE (= Visual Understanding Environment)](https://vue.tufts.edu/), an open source project of Tufts University.

## Classes and properties ##

**[Visualization of classes and properties](https://github.com/MiMoText/ontology/blob/main/Overview_classes-properties-datasets-federation.md#overview-1-classes-and-properties)**

### Classes ###

[annotation data set](https://data.mimotext.uni-trier.de/wiki/Item:Q3954) – 
[author](http://data.mimotext.uni-trier.de/wiki/Item:Q11) – [bibliography](http://data.mimotext.uni-trier.de/wiki/Item:Q13) – [concept](http://data.mimotext.uni-trier.de/wiki/Item:Q35) – [concept narrative form](http://data.mimotext.uni-trier.de/wiki/Item:Q37) – [concept tone](https://data.mimotext.uni-trier.de/wiki/Item:Q3890) – [concept intention](https://data.mimotext.uni-trier.de/wiki/Item:Q3892) – [controlled vocabulary](http://data.mimotext.uni-trier.de/wiki/Item:Q17) – [corpus](https://data.mimotext.uni-trier.de/wiki/Item:Q3955) – [data set](http://data.mimotext.uni-trier.de/wiki/Item:Q8) – [entity](http://data.mimotext.uni-trier.de/wiki/Item:Q9) – [fictional prose](http://data.mimotext.uni-trier.de/wiki/Item:Q12) – [human](http://data.mimotext.uni-trier.de/wiki/Item:Q10) – [general property](https://data.mimotext.uni-trier.de/wiki/Item:Q4054) – [(literary) genre](http://data.mimotext.uni-trier.de/wiki/Item:Q33) – [item(class)](http://data.mimotext.uni-trier.de/wiki/Item:Q14) – [literary work](http://data.mimotext.uni-trier.de/wiki/Item:Q2) – [mapping / identifying property](https://data.mimotext.uni-trier.de/wiki/Item:Q4056) – [matching table](http://data.mimotext.uni-trier.de/wiki/Item:Q29) – [NER_data set](https://data.mimotext.uni-trier.de/wiki/Item:Q28) –  [owl:Thing](http://data.mimotext.uni-trier.de/wiki/Item:Q16) – [property (class)](http://data.mimotext.uni-trier.de/wiki/Item:Q15) – [property for items about works](https://data.mimotext.uni-trier.de/wiki/Item:Q3891) – [property for items about persons](https://data.mimotext.uni-trier.de/wiki/Item:Q4057) –  [publication](http://data.mimotext.uni-trier.de/wiki/Item:Q7) – [referencing property](https://data.mimotext.uni-trier.de/wiki/Item:Q4055) – [scholarly book](https://data.mimotext.uni-trier.de/wiki/Item:Q3925) – [scholarly book section](https://data.mimotext.uni-trier.de/wiki/Item:Q3926) – [scholarly journal article](https://data.mimotext.uni-trier.de/wiki/Item:Q3927) – [scholarly work](http://data.mimotext.uni-trier.de/wiki/Item:Q3) – [sentiment analysis](https://data.mimotext.uni-trier.de/wiki/Item:Q4053) – [spatial concept](https://data.mimotext.uni-trier.de/wiki/Item:Q26) – [spatial vocabulary](http://data.mimotext.uni-trier.de/wiki/Item:Q31) – [stylometric analysis](https://data.mimotext.uni-trier.de/wiki/Item:Q4050) – [thematic concept](http://data.mimotext.uni-trier.de/wiki/Item:Q20) – [thematic vocabulary](http://data.mimotext.uni-trier.de/wiki/Item:Q30) – [topic](http://data.mimotext.uni-trier.de/wiki/Item:Q22) – [topic labels and concepts (11-2020)](http://data.mimotext.uni-trier.de/wiki/Item:Q34) – [topic model](http://data.mimotext.uni-trier.de/wiki/Item:Q18) – [vocabulary intention](https://data.mimotext.uni-trier.de/wiki/Item:Q3973) – [vocabulary narrative form](http://data.mimotext.uni-trier.de/wiki/Item:Q32) – [vocabulary tone](https://data.mimotext.uni-trier.de/wiki/Item:Q3972)

### Properties
(including qualifiers)

[about](http://data.mimotext.uni-trier.de/wiki/Property:P36) – [author](http://data.mimotext.uni-trier.de/wiki/Property:P5) – [author name string](http://data.mimotext.uni-trier.de/wiki/Property:P6) – [author of](http://data.mimotext.uni-trier.de/wiki/Property:P7) – [BGRF ID](http://data.mimotext.uni-trier.de/wiki/Property:P22) – [characters string](http://data.mimotext.uni-trier.de/wiki/Property:P29) – [BGRF_plot_theme](http://data.mimotext.uni-trier.de/wiki/Property:P30) – [BGRF_tone_intention](http://data.mimotext.uni-trier.de/wiki/Property:P31) – [characters string](https://data.mimotext.uni-trier.de/wiki/Property:P29) – [close match](http://data.mimotext.uni-trier.de/wiki/Property:P16) – [described at URL](http://data.mimotext.uni-trier.de/wiki/Property:P19) – [described by source](http://data.mimotext.uni-trier.de/wiki/Property:P20) – [distribution format string](http://data.mimotext.uni-trier.de/wiki/Property:P26) –  [DOI](https://data.mimotext.uni-trier.de/wiki/Property:P59) – [equivalent class](http://data.mimotext.uni-trier.de/wiki/Property:P15) – [equivalent property](http://data.mimotext.uni-trier.de/wiki/Property:P14) – [exact match](http://data.mimotext.uni-trier.de/wiki/Property:P13) – [full work available at URL](http://data.mimotext.uni-trier.de/wiki/Property:P21) – [genre](http://data.mimotext.uni-trier.de/wiki/Property:P12) – [has part(s)](https://data.mimotext.uni-trier.de/wiki/Property:P53) –[image](https://data.mimotext.uni-trier.de/wiki/Property:P54) – [instance of](http://data.mimotext.uni-trier.de/wiki/Property:P2) – [intention](https://data.mimotext.uni-trier.de/wiki/Property:P39) – [language of work or name](https://data.mimotext.uni-trier.de/wiki/Property:P57) – [mentioned in](https://data.mimotext.uni-trier.de/wiki/Property:P51) – [mentions](https://data.mimotext.uni-trier.de/wiki/Property:P50) –  [name](http://data.mimotext.uni-trier.de/wiki/Property:P8) – [narrative form](http://data.mimotext.uni-trier.de/wiki/Property:P33) – [narrative form string](http://data.mimotext.uni-trier.de/wiki/Property:P27) – [narrative location](http://data.mimotext.uni-trier.de/wiki/Property:P32) – [narrative location string](http://data.mimotext.uni-trier.de/wiki/Property:P28) – [number of pages string](http://data.mimotext.uni-trier.de/wiki/Property:P25) –  [occupation](http://data.mimotext.uni-trier.de/wiki/Property:P11) – [occurence in text](https://data.mimotext.uni-trier.de/wiki/Property:P41) – [part of](http://data.mimotext.uni-trier.de/wiki/Property:P37) – [place of publication](http://data.mimotext.uni-trier.de/wiki/Property:P10) – [place of publication string](http://data.mimotext.uni-trier.de/wiki/Property:P24) – [publication date](http://data.mimotext.uni-trier.de/wiki/Property:P9) – [publication date string](http://data.mimotext.uni-trier.de/wiki/Property:P23) – [published in](https://data.mimotext.uni-trier.de/wiki/Property:P43) – [published in string](https://data.mimotext.uni-trier.de/wiki/Property:P44) – [quotation](https://data.mimotext.uni-trier.de/wiki/Property:P42) – [reference image](https://data.mimotext.uni-trier.de/wiki/Property:P55) – [reference URL](http://data.mimotext.uni-trier.de/wiki/Property:P17) – [related to](http://data.mimotext.uni-trier.de/wiki/Property:P34) – [represented by](http://data.mimotext.uni-trier.de/wiki/Property:P35) – [sentiment arc diagram](https://data.mimotext.uni-trier.de/wiki/Property:P58) – [stated in](http://data.mimotext.uni-trier.de/wiki/Property:P18) – [stylometric based similarity](https://data.mimotext.uni-trier.de/wiki/Property:P49) – [stylometric distance value](https://data.mimotext.uni-trier.de/wiki/Property:P52) – [subclass of](http://data.mimotext.uni-trier.de/wiki/Property:P1) – [subproperty of](http://data.mimotext.uni-trier.de/wiki/Property:P3) – [title](http://data.mimotext.uni-trier.de/wiki/Property:P4) –  [tone](https://data.mimotext.uni-trier.de/wiki/Property:P38) – [topic interest](https://data.mimotext.uni-trier.de/wiki/Property:P47)

## Modeling approach & decisions
We are not attempting to model the entire domain of literary history and historiography deductively, but rather based on our purpose to connect inductively the different data source types.
Where possible and necessary, for example in the case of the narrative form, we have conceptually addressed the corresponding theoretical concepts and strived for a mediation that increases plausibility and acceptance among literary scholars. Each module, which has only been visualized so far, is explained and more detail in the various decisions made in the modeling process.

## Infrastructure & prefixes

### Open Science
For the provision of data, we follow open science principles, such as the publication of FAIR data in open access as well as the use of open source software – in particular Wikibase. We created a [custom bot using the Python library Pywikibot](https://github.com/MiMoText/Wikibase-Bot) to import and update the RDF triples into our Wikibase instance from TSV files. Towards the end of the project, we also used [QuickStatements](https://www.wikidata.org/wiki/Help:QuickStatements) to import data.

### Wikibase ecosystem
We understand our [MiMoTextBase](https://docs.mimotext.uni-trier.de) as [part of the Wikibase ecosystem](https://github.com/MiMoText/ontology/blob/main/module13_federation/wikibase_ecosystem.png) with the decision for a self-hosted Wikibase instance. The infrastructure of a Wikibase has a significant influence on the data model and therefore also on the query possibilities.

### Prefixes 
Regarding the prefixes, we have decided to stay within the Wikidata logic of the labeling to increase usability for those who are already familiar with the Wikidata prefixes (e.g. 'mmd' for the 'entities' instead of 'wd', 'mmdt' for the 'properties' instead of 'wdt').

- mmd: http://data.mimotext.uni-trier.de/entity/
- mmdt: http://data.mimotext.uni-trier.de/prop/direct/
- mmps: http://data.mimotext.uni-trier.de/prop/statement/
- mmpr: http://data.mimotext.uni-trier.de/prop/reference/
- mmds: http://data.mimotext.uni-trier.de/entity/statement/
- mmdv: http://data.mimotext.uni-trier.de/value/
- mmdref: http://data.mimotext.uni-trier.de/reference/
- mmdtn: http://data.mimotext.uni-trier.de/prop/direct-normalized/
- mmp: http://data.mimotext.uni-trier.de/prop/
- mmdno: http://data.mimotext.uni-trier.de/prop/novalue/
- mmps: http://data.mimotext.uni-trier.de/prop/statement/
- mmpsv: http://data.mimotext.uni-trier.de/prop/statement/value/
- mmpsn: http://data.mimotext.uni-trier.de/prop/statement/value-normalized/
- mmpq: http://data.mimotext.uni-trier.de/prop/qualifier/
- mmpqv: http://data.mimotext.uni-trier.de/prop/qualifier/value/
- mmpqn: http://data.mimotext.uni-trier.de/prop/qualifier/value-normalized/
- mmpr: http://data.mimotext.uni-trier.de/prop/reference/
- mmprv: http://data.mimotext.uni-trier.de/prop/reference/value/
- mmprvn: http://data.mimotext.uni-trier.de/prop/reference/value-normalized/
- mmdata: http://data.mimotext.uni-trier.de/Special:EntityData/

For a visualization of our data model see the [ABOUT-page](https://mimotext.github.io/MiMoTextBase_Tutorial/aboutMiMoTextBase.html) of our tutorial (under: "MiMoText SPARQL data Representation and how to access different statement types") based on the  [Wikidata / Wikibase data model](https://en.wikibooks.org/wiki/SPARQL/WIKIDATA_Qualifiers,_References_and_Ranks#/media/File:SPARQL_data_representation.png). 

### Queries Overview Ontology
Here are some queries that provide an overview of different aspects of the MiMoText ontology.

- [Properties structure](https://tinyurl.com/2asuq499)
- [Classes structure](https://tinyurl.com/2dynwyew)
- [Data sets structure](https://tinyurl.com/28aoojfg)
- [Controlled vocabularies](https://query.mimotext.uni-trier.de/#%23Overview%20over%20our%20controlled%20vocabulary%0A%23title%3AOverview%20over%20controlled%20vocabularies%0A%23%20Query%20to%20retrieve%20the%20different%20controlled%20vocabularies%0APREFIX%20mmd%3A%20%3Chttp%3A%2F%2Fdata.mimotext.uni-trier.de%2Fentity%2F%3E%0APREFIX%20mmdt%3A%20%3Chttp%3A%2F%2Fdata.mimotext.uni-trier.de%2Fprop%2Fdirect%2F%3E%0A%0ASELECT%20%3Fvoc%20%3FvocLabel%20%28COUNT%28%3FvocLabel%29%20as%20%3Fcount%29%20%28COUNT%28%3Fwikimatch%29%20as%20%3Fwikimatch%29%0AWHERE%20%7B%0A%20%20%20%3Fitem%20mmdt%3AP37%20%3Fvoc.%0A%20%20%20%3Fvoc%20mmdt%3AP2%2Fmmdt%3AP1%20mmd%3AQ17.%0A%20%20%20OPTIONAL%7B%0A%20%20%20%20%20values%20%3Fwiki%20%7Bmmdt%3AP13%20mmdt%3AP16%7D%0A%20%20%20%20%20%3Fitem%20%3Fwiki%20%3Fwikimatch%7D%0A%20%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%20%20%7D%0AGROUP%20BY%20%3Fvoc%20%3FvocLabel%0AORDER%20BY%20DESC%28%3Fcount%298)
- [Multilingual classes and their descriptions](https://tinyurl.com/28d3hgk7)
- [Multilingual properties and their descriptions](https://tinyurl.com/2b68fhl6)
- [Multilingual datasets and their descriptions](https://tinyurl.com/2dydvllg)

The queries address our MiMoTextBase / Wikibase query interface ([https://query.mimotext.uni-trier.de](https://query.mimotext.uni-trier.de)). The actual SPARQL endpoint can be found under the following link:  [https://query.mimotext.uni-trier.de/proxy/wdqs/bigdata/namespace/wdq/sparql](https://query.mimotext.uni-trier.de/proxy/wdqs/bigdata/namespace/wdq/sparql).

### Linking with the Wikidata-Graph
In the context of linking our graph within the 'Wikibase ecosystem' we have planned and realized several steps. The [interview with Wikimedia Germany](https://tech-news.wikimedia.de/en/2024/06/28/modeling-the-enlightenment-novel-an-interview-with-the-mimotext-team/) summarizes our main steps towards bidirectional federation between MiMoTextBase and Wikidata. 

* mapping of thematic and spatial concepts in our controlled vocabularies (done).
* mapping of properties and classes (done)
* mapping of author and work items (done)
* creation of a MiMoText ID in Wikidata (done)
* linking the literary works we could map from Wikidata to the work items in our MiMoTextBase (done)
* importing the work and author items not yet available in Wikidata into Wikidata and also linking them to our MiMoTextBase. (done)
* request for whitelisting of MiMoTextBase as SPARQL endpoint queryable from Wikidata (done)

Beyond that we would be happy to have the opportunity to link our data in the sense of Linked Open Data to further ressources / authority data (VIAF, GND e.g.). For pragmatic reasons we focused on Wikidata so far. 

### Formal representation
This repository addresses so far mainly the conceptual representation. The ontology is part of the MiMoTextBase and downloadable as an [RDF Dump of the MiMoTextBase](https://doi.org/10.5281/zenodo.10021150) for further reuse.
We were thinking about making the overall ontology as well as the individual modules available as OWL files, also depending on feedback about possible usage scenarios. This step could not be realized by the end of the project.

### Related work
With regard to reuse and mapping, we have so far focused on Wikidata, which we see as a kind of 'hub'. In the development of the ontology, we have explored other projects in or neighboring our domain and tried to integrate solution approaches, if they were transferable, into our modeling (e.g. [ArtBase](https://artbase.rhizome.org/wiki/Main_Page), [ONAMA](http://onama.sbg.ac.at), [Enslaved.org](https://enslaved.org/), [Krater/O4DH](http://o4dh.com/datasets), [GOLEM](https://golemlab.eu/). The [ELTeC project](https://www.distant-reading.net/eltec/) is particularly related, insofar as it also involves modeling novel data in Wikidata (Ikonić Nešić et al. 2021). However, while in European Literary Text Collection (ELTeC) the differentiation between the literary work and different edition versions is very important, we have decided to put the literary work in the center and to avoid further differentiations within our MiMoTextBase in order to reduce complexity.

### Reification & inference
We have so far focused mainly on referencing (see referencing module) and conceptualized to use simple qualifiers (e.g. counting text occurrences with the property "occurence in text"). We have not yet made use of all the potential of the Wikibase infrastructure, for example, for ranking statements or modeling different reliabilities of statements. However, we have discussed this in the context of ranking topics for more precise modeling of thematic statements based on topic modeling.
The question of inferring statements from other statements (implicit statements) is different within the data model of Wikibase (and our ontology working with it) than in ontologies that follow the OWL standards more strictly and in particular make a clear separation of classes and instance data ('individuals'). This separation does not exist in the Wikibase infrastructure per se (but can be constructed via statements), which has consequences for inferences (which are nevertheless possible).


## Community
An ontology is not an ontology as long as it is only used in one project. We therefore see it rather as an ontology proposal. We would like to discuss our modeling decisions in exchange with colleagues from Computational Literary Studies as well as other fields of Digital Humanities in order to jointly develop the ontology for the community, i.e. a data model that can structure information in different projects and link them in the spirit of Linked Open Data.
We would also like to get in closer contact with literary scholars to extend the modeling of the relevant types of statements we have identified.

## Licence (CC-0)
All data modeling is in the public domain and can be reused without restrictions. We don’t claim any copyright or other rights. If you use the ontology, for example in research or teaching, please reference this ontology using the citation suggestion below.

## Citation Suggestion
MiMoText ontology, edited by Maria Hinzmann, with contributions from Matthias Bremm, Tinghui Duan, Anne Klee, Johanna Konstanciak Julia Röttgermann, Christof Schöch and Moritz Steffes. Release v1.1.0. Trier: TCDH, 2024. URL: https://github.com/MiMoText/ontology

## Related Ressources
- [MiMoTextBase - a knowledge graph on Eighteenth Century French Novels](https://data.mimotext.uni-trier.de)
- [MiMoText SPARQL endpoint (Query Service)](https://query.mimotext.uni-trier.de)
- [MiMoText SPARQL tutorial](https://docs.mimotext.uni-trier.de)
- [interview with Wikimedia Germany](https://tech-news.wikimedia.de/en/2024/06/28/modeling-the-enlightenment-novel-an-interview-with-the-mimotext-team/)
- [MiMoTextBase Tutorial: How to query the graph and an introduction to SPARQL] https://docs.mimotext.uni-trier.de)
- [MiMoText vocabularies](https://github.com/MiMoText/vocabularies)
- [RDF Dump MiMoTextBase](https://doi.org/10.5281/zenodo.10021150)

## Bibliography
* Arenas, Marcelo, Claudio Gutierrez, and Jorge Pérez. 2010. “On the Semantics of SPARQL.” In Semantic Web Information Management: A Model-Based Perspective, edited by Roberto de Virgilio, Fausto Giunchiglia, and Letizia Tanca, 281–307. Berlin, Heidelberg: Springer. https://doi.org/10.1007/978-3-642-04329-1_13.
* Bremm, Matthias, Tinghui Duan, Maria Hinzmann, Anne Klee, Johanna Konstanciak, Julia Röttgermann, Christof Schöch, and Moritz Steffes. “MiMoTextBase RDF Dump.” Zenodo, September 20, 2024. https://doi.org/10.5281/zenodo.13825346.
* Eells, Andrew, Cogan Shimizu, Lu Zhou, Pascal Hitzler, and Dean Rehberger. 2021. “Aligning Patterns to the Wikibase Model.” In Http://Ontologydesignpatterns.Org/Wiki/WOP:2021. https://daselab.cs.ksu.edu/sites/default/files/WOP2021_paper_4.pdf.
* Gangemi, Aldo, and Valentina Presutti. 2009. “Ontology Design Patterns.” In Handbook on Ontologies, 221–43. https://doi.org/10.1007/978-3-540-92673-3_10.
* Gruber, Thomas R. 1995. “Toward Principles for the Design of Ontologies Used for Knowledge Sharing?” International Journal of Human-Computer Studies 43 (5): 907–28. https://doi.org/10.1006/ijhc.1995.1081.
* Hinzmann, Maria, Matthias Bremm, Tinghui Duan, Anne Klee, Johanna Konstanciak, Julia Röttgermann, Christof Schöch, and Joëlle Weis. “Patterns in Modeling and Querying a Knowledge Graph for Literary History (Preprint).” https://doi.org/10.5281/zenodo.12080340.
* Hitzler, P. 2021. “A Review of the Semantic Web Field.” Commun. ACM. https://doi.org/10.1145/3397512.
* Hitzler, P., M. Krötzsch, and S. Rudolph. 2009. “Foundations of Semantic Web Technologies.” In . https://doi.org/10.1201/9781420090512.
* Hitzler, Pascal, Aldo Gangemi, Krzysztof Janowicz, Adila Krisnadhi, and Valentina Presutti, eds. 2016. Ontology Engineering with Ontology Design Patterns: Foundations and Applications. Studies on the Semantic Web, vol. 025. Berlin, Germany : Amsterdam, Netherlands: Akademische Verlagsgesellschaft ; IOS Press.
* Ikonić Nešić, Milica, Ranka Stanković, and Biljana Rujević. 2021. “Serbian ELTeC Sub-Collection in Wikidata.” Infotheca 21 (2): 60–86. https://doi.org/10.18485/infotheca.2021.21.2.4.
* Janowicz, Krzysztof, Aldo Gangemi, Pascal Hitzler, Adila Krisnadhi, and Valentina Presutti. 2016. “Introduction: Ontology Design Patterns in a Nutshell.” In Ontology Engineering with Ontology Design Patterns: Foundations and Applications, edited by Pascal Hitzler, Aldo Gangemi, Krzysztof Janowicz, Adila Krisnadhi, and Valentina Presutti. Studies on the Semantic Web, vol. 025. Berlin, Germany : Amsterdam, Netherlands: Akademische Verlagsgesellschaft ; IOS Press. https://people.cs.ksu.edu/~hitzler/pub2/00-introduction.pdf.
* Noy, Natalya F., and Deborah L. McGuinness. 2001. “Ontology Development 101: A Guide to Creating Your First Ontology.” https://protege.stanford.edu/publications/ontology_development/ontology101.pdf.
* Röttgermann, Julia, and Christof Schöch. 2020. “FAIRe Daten in Den Literaturwissenschaften? Das Beispiel „Mining and Modeling Text“ Und Der Französische Roman Des 18. Jahrhunderts.” Romanistik-Blog. Blog des Fachinformationsdienstes (blog). 2020. https://blog.fid-romanistik.de/2020/11/05/faire-daten-in-den-literaturwissenschaften/.
* Shimizu, Cogan, Andrew Eells, Seila Gonzalez, Lu Zhou, Pascal Hitzler, Alicia Sheill, Catherine Foley, and Dean Rehberger. 2024. “Ontology Design Facilitating Wikibase Integration — and a Worked Example for Historical Data.” Journal of Web Semantics 82 (October):100823. https://doi.org/10.1016/j.websem.2024.100823.
* Shimizu, Cogan, Karl Hammar, and Pascal Hitzler. 2023. “Modular Ontology Modeling.” Edited by Sabrina Kirrane, Axel-Cyrille Ngonga Ngomo, Sabrina Kirrane, and Axel-Cyrille Ngonga Ngomo. Semantic Web 14 (3): 459–89. https://doi.org/10.3233/SW-222886.
