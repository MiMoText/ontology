# Federation between MiMoTextBase and Wikidata

This module represents the modeling decisions that were relevant to enable federation between the [MiMoTextBase](https://data.mimotext.uni-trier.de) (Wikibase instance of the "Mining and Modeling Text", short "MiMoText" project) and Wikidata. Both knowledge graphs can be queried in combination with federated queries (for examples, see the [section in our tutorial](https://mimotext.github.io/MiMoTextBase_Tutorial/federated.html) and below).

## Why 'federated queries'? 
Federation plays a crucial role in realizing the potential of the Linked Open Data paradigm. The basic idea is to overcome separate data silos in which information is stored redundantly. Instead, the Linked Open Data Cloud contains knowledge that has been created in very different contexts and is linked together in the cloud. Ideally, a particular dataset can be supplemented by information from other datasets; and conversely, your own data is no longer isolated, but part of and a contribution to the Linked Open Data Cloud. Federated queries are relevant in order to be able to use these links in the global Semantic Web. These are formulated in the SPARQL query language. While SPARQL queries can generally also address only one knowledge graph, federated queries make it possible to address several SPARQL endpoints simultaneously.

## The Wikibase ecosystem
We chose a local instance of Wikibase as the infrastructure for our data in MiMoText for several reasons (see the [about-section of our tutorial](https://mimotext.github.io/MiMoTextBase_Tutorial/aboutMiMoTextBase.html) for more information). Wikidata as the largest Wikibase instance is of great importance as a kind of “hub” for linking humanities data across project boundaries. The more projects in this ecosystem share the same infrastructure, the denser and more significant the whole graph becomes. Federated queries are of course possible across different types of infrastructures (via RDF and SPARQL as W3C standards) but are clearly made easier by a common basic data model as it is shared via Wikibase. We see the MiMoTextBase as part of the growing Wikibase ecosystem. The more projects in this ecosystem share the same infrastructure, the denser and more significant the whole graph becomes. With the Wikibase infrastructure, we are embedded in a larger framework and share the data model with Wikidata as the largest public Wikibase instance. Federated queries are of course possible across different types of infrastructures but are clearly made easier by a common basic data model (e.g. modeling of [references](https://github.com/MiMoText/ontology/blob/main/Modules%20overview.md#module-7-referencing).


Figure: Wikibase Ecosystem

## MiMoTextBase and Wikidata: Modeling the connection of both knowledge graphs
We contributed a part of our data to Wikidata and linked both knowledge graphs to enable federation. A guiding idea was that some of the data on the 18th century French novel generated in our project is quite relevant to the general public, but some of it is also very specific. Following the logic of the ecosystem, we built up our MiMoTextBase step by step, shared a relevant part of the data with Wikidata and linked them in both directions. More specific data can be found in the MiMoTextBase. Using 'federated queries', more general data from Wikidata (e.g. the geo-coordinates of locations) can be used in the MiMoTextBase queries. On the other hand, Wikidata users can use the more specific information in the MiMoTextBase via 'federation'. Both knowledge graphs are linked to each other in the Wikibase ecosystem, where the basic data model of the Wikibase infrastructure is shared, but also beyond that in the Linked Open Data Cloud or the Semantic Web.
The simple alignment of single entities across knowledge bases (here with "exact match" or the "MiMoText ID"), which enables federated queries, is an important step and already extremely useful, even without exhausting all the possibilities originally envisioned in the Semantic Web (of reasoning and inferencing etc.). The following visulization gives an overview about the types of entities ("classes") which are matched and the data that was shared with Wikidata. To get more information on more specific decisions see the visualization for [module 13](https://github.com/MiMoText/ontology/blob/main/Modules%20overview.md#module-13-federation).


Figure: Federation Overview

## The process

### Creating the MiMoTextID as external identifier in Wikidata

In our knowledge graph MiMoTextBase, every item of a work or a person is provided with a stable Uniform Resource Identifier (URI) consisting of a Q and a numeric identifier, for example Q1053. We chose to propose this identifier to the Wikidata community as well. 
The first step is using this [link](...) and formulating the proposal. The process of proposing a [MiMoTextID](https://www.wikidata.org/wiki/Property:P12047) as a Wikidata property implies e.g. formulating a formatter ID (https://data.mimotext.uni-trier.de/wiki/Item:$1). 
Bevor wir den [Proposal für die MiMoText ID](https://www.wikidata.org/wiki/Wikidata:Property_proposal/MiMoText_ID) submitted, 
Before submitting the proposal, we contacted Wikimedia Deutschland to discuss and clarify the process. Alan Ang and Christos Varvantakis advized us to gather feedback on the proposal from the community (via the Wikidata Telegram channel) and briefly outline the background to the community. This was very helpful and our property proposal for the creation of a MiMoTextID on Wikidata was accepted on 28 September 2023 by the community. 
This MiMoTextID allows linking Wikidata items back to our knowledge graph, to make the linking of resources explicit in both ways and as a side effect, may allow Wikidata users to discover the rich resources on these items in the MiMoText knowledge graph.  
Furthermore, adding Wikidata identifiers to MiMoTextbase and adding MiMoTextID to Wikidata items as statements is a precondition for the functioning of federated queries.
To be fully machine readable, it has to be expressed in an RDF statement that ‘Les liaisons dangereuses’ on MiMoTextBase and ‘Les liaisons dangereuses’ on Wikidata both mean the same literary work (see Fig. I). The reconciliation of the works was done on the level of the literary work, not on the level of an edition or a collection. However, if an item already existed as an “edition, version or translation of”, we created a “literary work” and linked it to the existing item. However, our data are all related to “literary work” items, as is also the case in the MiMoTextBase.

Figure: The data item ‘Les liaisons dangereuses’ Q862050 on Wikidata with identifier MiMoTextID

There are now 812 literary works available on Wikidata, that have a MiMoTextID. Which novels on Wikidata do have a MiMoTextID? https://w.wiki/8UC$

### Criteria for selection a subset of MiMoText novels to be represented in Wikidata

We wanted to avoid redundancies in the Wikibase ecosystem and at the same time enable a bridge between Wikidata and MiMoTextBase that allows users with an interest in the MiMoTextBase domain (French Novel, Enlightenment etc.) to become aware of the MiMoTextBase and to include this data in federated queries. To link MiMoTextBase-Items to Wikidata, we created the property “exact match” (https://data.mimotext.uni-trier.de/wiki/Property:P13) and imported the corresponding URLs of the wikidata items into the MiMoTextBase. Since we do not assume that all of the approximately 1750 novels in the MiMoTextBase are relevant to the Wikidata public, we have come up with internal relevance criteria.
Nearly all items that are within the MiMoTextBase are based on the entries found in the Bibliographie du genre romanesque français 1751-1800 (Martin, Mylne and Frautschi, 1977), in short “BGRF”. For those we were able to extract different kinds of statements to varying degrees, such as publication date, place of publication, strings on characters found in the novels, plot, theme etc. For a subcorpus of 200 full texts (https://doi.org/10.5281/zenodo.10276850) built within the project, we were able to generate further statements based on computational methods. A third source of statements is a corpus of secondary literature that was annotated and analyzed. These elements combined formed the basis for deciding which works we wanted to import into Wikidata. Items for which full texts were available should definitely be imported; for a further selection, we defined additional criteria (see below). Due to this two groups of novels, the steps for the import can be differentiated as follows.

### Imports / Edits of Statements in Wikidata

=> Creating and Editing Items with QuickStatements and via OpenRefine (#)

#### roman18-corpus 
As we created a corpus of about 200 fulltext novels within the project that is based on different balancing criteria (e.g. year of creation, narrative form, gender) to represent the overall novels of around 2000 that were written during the period 1751-1800, we were able to perform different computational methods of analyzing these texts such as topic modeling and Named Entity Recognition (see: https://github.com/MiMoText/roman18).
As some of these novels are canonical work, they already had an existing wikidata entry, such as “Candide” (https://www.wikidata.org/wiki/Q215894), in which case we only wanted to import further statements to these entries. While encoding the texts in XML-TEI format, we also already included the Wikidata-ID, where possible, in the file header. For the lesser known works where we didn’t find a wikidata entry or where only items that are instance of “version, edition or translation” (https://www.wikidata.org/wiki/Q3331189), we created new items and populated them with statements from the MiMoTextBase and referenced these with the corresponding items. 

Statements that we either created or extended are:
title, author, year of publication, narrative location, main subject, full text URL, MiMoText-ID.

#### Novels which are not part of the roman18-corpus

As we generally did not want to import all works from the MiMoTextBase into wikidata, we defined various relevance criteria for the next import step. We decided to import only those works into wikidata that have statements on both topics and narrative locations, which in turn are referenced by the BGRF or secondary literature. Furthermore, at least 3 such statements should be linked to the work, see query [here](http://tinyurl.com/yt5sk3xc). The import process was split on the condition whether the author was known or the work was published anonymously.


## Queries: examples

The W3C defines 'federated queries' as follows: "SPARQL can be used to express queries across diverse data sources, whether the data is stored natively as RDF or viewed via middleware." The Wikibase software is such a middleware, so that a distinction can be made between access via the Wikibase / MiMoTextBase Query Service (query.mimotext.uni-trier.de) and access via the actual endpoint (...). 
The Query Service has a great number of possibilities to download the results in several format, implement the queries in your code or visualize the results. The following selection of queries uses the MiMoTextBase and Wikidata Query Service and demonstrates how federated queries can be performed on both knowledge graphs. One can formulate property constraints. 
Our property proposal for the creation of a MiMoTextID on Wikidata was accepted on 28 September 2023 by the community. 

=> Example-Queries federation -> PURL domain (#)

### MiMoTextBase - Wikidata

Example Query 1

Example Query 2

### Wikidaeta - MiMoTextBase

Example Query 1

Example Query 2


