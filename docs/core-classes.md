---
layout: single
title: Core Classes
permalink: /docs/core-classes/
sidebar:
  nav: "docs"
---

The top-level organization of the main classes of the ontology conforms to the Basic Formal Ontology (BFO) upper ontology as shown in the following figure:

![Basic Class Hierarchy](/assets/images/docs/journal.pone.0154556.g001.PNG)

This provides a basic model for how OBI structures a theoretical description of experimental methodology.  Although this view is quite complicated, much of the design of OBI revolves round four classes: (A) [`planned process`](http://purl.obolibrary.org/obo/OBI_0000011)
(B) [`plan specification`](http://purl.obolibrary.org/obo/IAO_0000104), (C) [`material entity`](http://purl.obolibrary.org/obo/BFO_0000040), and (D) [`information content entity`](http://purl.obolibrary.org/obo/IAO_0000030). 

OBI's scheme for generating linked data that describe experiments (at least down to the protocol level) is illustrated in the following figure: 

![Domains and Ranges for Object Properties](/assets/images/docs/obi_schema.png)

Any [`planned process`](http://purl.obolibrary.org/obo/OBI_0000011) can specify substructure through the [`has part`](http://purl.obolibrary.org/obo/BFO_0000051) object property. Usually an [`investigation`](http://purl.obolibrary.org/obo/OBI_0000066) is the focus of our interest, and is linked to a [`study design execution`](http://purl.obolibrary.org/obo/OBI_0000471) that may then be made up of individuals made from three classes of processes that are used in scientific protocols: [`material processing`](http://purl.obolibrary.org/obo/OBI_0000094), [`assay`](http://purl.obolibrary.org/obo/OBI_0000070), and [`information content entity`](http://purl.obolibrary.org/obo/OBI_0200000). 

We then use the `has specified input` and `has specified output` object properties to link these processes to either [`material entity`](http://purl.obolibrary.org/obo/BFO_0000040) or [`data item`](http://purl.obolibrary.org/obo/IAO_0000027) objects to describe a complete experimental scientific protocol. The actual values of data elements in OBI are mainly provided by instances of the [`value specification`](http://purl.obolibrary.org/obo/OBI_0001933) class. We may also specify the conclusions of a study through the [`drawing a conclusion based on data`](http://purl.obolibrary.org/obo/OBI_0000338) process which generates a [`conclusion based on data`](http://purl.obolibrary.org/obo/OBI_0001909). Additional semantics are invoked to instantiate these models for real data, but these core classes provide the basic structure for such descriptions. 

<!-- An example of the use of this architecture to specify a protocol in the molecular biology space will be forthcoming below. -->

   