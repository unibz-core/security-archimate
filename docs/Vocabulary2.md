---
title: Vocabulary2
layout: home
---



## Usage Guide <a name="usageguide"></a>

### Table of Contents

* 1\. [Usage Scenarios](#scenarios)
* 2\. [Taxonomy of Individuals](#individuals)
    * 2.1\. [Concrete Individuals](#concreteindividuals)
    * 2.2\. [Objects and their parts](#objectsandparts)
    * 2.3\. [Intrinsic Aspects](#intrinsicaspects)
    * 2.4\. [Qualities - Basic patterns](#basicqualities)
    * 2.5\. [Qualities - Advanced usage](#advancedqualities)
    * 2.6\. [Intrinsic Modes](#intrinsicmodes)
    * 2.7\. [Extrinsic Aspects](#extrinsicaspects)
    * 2.8\. [Events](#events)
    * 2.9\. [Situations](#situations)
* 3\. [Taxonomy of Types](#types)
    * 3.1\. [Endurant Types](#enduranttypes)
    * 3.2\. [Relationship Types](#relationshiptypes)
    * 3.3\. [Higher-Order Types](#highordertypes)

See also [reference table of contents](#toc).

<a name="scenarios"></a>

### 1. Usage Scenarios

gUFO is intended for reuse in the definition of UFO-based lightweight ontologies. The term "user" will thus be reserved to identify the designers of these ontologies.

Reuse of gUFO consists in instantiating and/or specializing the  various classes, object properties and data properties defined in the ontology, inheriting from it the domain-independent distinctions of UFO. This section provides an introduction to gUFO as a primer to prospective users. [Turtle](https://www.w3.org/TR/turtle/) is used as a syntax for RDF serialization for illustrative purposes.  

A key feature of UFO (and hence, gUFO) is that it includes two taxonomies: one with classes whose instances are individuals (classes in this taxonomy include gufo:Object, gufo:Event) and another with classes whose instances are types (classes in this taxonomy include gufo:Kind, gufo:Phase, gufo:Category).

An overview of these taxonomies in gUFO is shown below.

> * Individual
>     * AbstractIndividual
>     * ConcreteIndividual
>         * Endurant
>             * Object
>             * Aspect
>         * Event
>         * Situation
> * Type
>     * AbstractIndividualType
>     * ConcreteIndividualType
>         * EndurantType
>             * Sortal
>                 * Kind
>                 * Phase
>                 * Role
>                 * SubKind
>             * NonSortal
>                 * Category
>                 * PhaseMixin
>                 * RoleMixin
>                 * Mixin
>         * EventType
>         * SituationType
>     * RelationshipType

Considering these two taxonomies, the following usage scenarios are envisioned and discussed in this document  where appropriate:

1. A UFO-based ontology *instantiates* gUFO classes in the taxonomy of individuals  
   For example, `:Earth rdf:type gufo:Object` and `:WorldCup1970Final rdf:type gufo:Event`.
2. A UFO-based ontology *specializes* gUFO classes in the taxonomy of individuals  
   For example, `:Planet rdfs:subClassOf gufo:Object` and `:SoccerMatch rdfs:subClassOf gufo:Event`.
3. A UFO-based ontology *instantiates* gUFO classes in the taxonomy of types  
   For example, `:Planet rdf:type gufo:Kind`, `:Child rdf:type gufo:Phase`.
4. A UFO-based ontology *specializes* gUFO classes in the taxonomy of types  
   For example, `:PersonPhase rdfs:subClassOf gufo:Phase`.

Users may combine the various scenarios discussed. For example, users will often employ scenarios 2 and 3 in combination as shown in the following fragment, which defines a "Person" class that specializes gufo:Object and instantiates gufo:Kind:

    @prefix : <http://purl.org/nemo/example#> .
    @prefix gufo: <http://purl.org/nemo/gufo#> .

    :Person rdf:type owl:Class ;
            rdfs:subClassOf gufo:Object ;
            rdf:type gufo:Kind .

<a name="individuals"></a>

### 2. Taxonomy of Individuals

The taxonomy of individuals of gUFO has the following overall structure:

> * Individual
>     * AbstractIndividual
>     * ConcreteIndividual
>         * Endurant
>             * Object
>             * Aspect
>         * Event
>         * Situation

<a name="concreteindividuals"></a>

#### 2.1. Concrete Individuals

A gufo:ConcreteIndividual, differently from a gufo:AbstractIndividual, is one that exists in space-time. Concrete individuals comprise objects (the Mount Everest, John, his car, the Brazilian 1988 Constitution), reified aspects of concrete individuals (John's height, his service agreement with Amazon, Inc.), events (the 1986 Mexico City Earthquake, the 2009 United Nations Climate Change Conference) and situations (the situation in which John weighs 80 kilograms, the situation in which Mary is a professor).

Together, objects and aspects form what we call endurants, as they are those concrete individuals that endure in time and may change qualitatively while keeping their identity. A gufo:Aspect is a characteristic or trait of a concrete individual that is itself conceived as an individual. Treating aspects as endurants (i.e., reifying aspects) allows us to consider the properties of aspects themselves, and track their change in time.

gUFO includes a number of data and object properties that can be used with concrete individuals. For example, temporal aspects of concrete individuals can be captured with the data properties gufo:hasBeginPointInXSDDate, gufo:hasBeginPointInXSDDateTimeStamp, gufo:hasEndPointInXSDDate and gufo:hasEndPointInXSDDateTimeStamp. In the case of objects (and aspects), these properties determine the time point when the object (or aspect) comes into existence or ceases to exist. In the case of events, these properties determine the time point when the event starts to take place or when it ends. In the case of situations, the properties determine the time point when the situation begins and ceases to hold. (Temporal instants may also be reified using time:Instant in which case the gufo:hasBeginPoint and gufo:hasEndPoint object properties are applicable, see [OWL-Time](https://www.w3.org/TR/owl-time/) for details concerning time:Instant, including support for Allen relations, temporal reference systems, temporal precision.)

For example, the 1985 Mexico City Earthquake started at 13:17:50 (UTC) on the 19th Sept. 1985 (scenario 1):

    :1985MexicoCityEarthquake rdf:type  gufo:Event ;
                       gufo:hasBeginPointInXSDDateTimeStamp "1985-09-19T13:17:50Z"^^xsd:dateTimeStamp .

By declaring Earthquake to be a sub-class of gufo:Event, the applicable object and data properties can be used with instances of earthquake (scenario 2):

    :Earthquake rdf:type owl:Class ;
                rdfs:subClassOf gufo:Event .

    :1985MexicoCityEarthquake rdf:type  :Earthquake ;
                            gufo:hasBeginPointInXSDDateTimeStamp "1985-09-19T13:17:50Z"^^xsd:dateTimeStamp .

gUFO also includes a number of part-whole relations for concrete individuals. See [gufo:isProperPartOf][] and its sub-properties.

<a name="objectsandparts"></a>