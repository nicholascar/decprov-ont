# DecProv-O
The Decision Provenance ontology


## Introduction
This ontology is for modelling decisions and thus the causes for actions or the use or generation of things. It allows for a better understanding of *why* something might have taken place, have been used or produced than the more generic [PROV ontology](https://www.w3.org/TR/prov-o/), on which it is mainly based, does.  

The specialised decision modelling elements of this ontology have been derived from the [W3C Decisions and Decision-Making Incubator Group](https://www.w3.org/2005/Incubator/decision/)'s Decision Ontology (DO) which can be found at <https://github.com/nicholascar/decision-o>. Many DO classes have been aligned with the PROV-O since it is widely recognised that analysing the elements of decisions *post hoc* is an exercise in provenance.

Unlike the original DO, this ontology cannot be used for *normative* scenarios: it is only capable of recording decisions that have already been made (so-called *data-driven* use in the DO). This is because PROV does not have a templating system which can indicate what *should* occur in future scenarios.

This ontology introduces only one new element for decision modelling over that which was present in the DO: an Agent which allows agency in decision making to be recorded.


## Ontology document
Namespace location:
* HTML: <http://promsns.org/def/decprov>
* RDF turtle: <http://promsns.org/def/decprov.ttl>

Local copies:
* HTML: [decprov.html](decprov.html)  
* RDF Turtle: [decprov.ttl](decprov.ttl)


## Ontology class diagram
![](images/decprov.png)  
All relationships are PROV-O relationships

## Modelling description
See [MODELLING](MODELLING.md) for a description of the choices made about classes in DecPROV, including why certain Decision Ontology classes were included, excluded or changed.


## Examples
See [EXAMPLES](EXAMPLES.md).


## Publications
* [Modelling causes for actions with the Decision and PROV ontologies (MODSIM 2017 conference)](http://github.com/nicholascar/decprov-ont/blob/master/references/Car2017-Modelling-causes-for-actions-with-the-Decision-and-PROV-ontologies.pdf)


## License
This ontology and all other content in this repository are licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) (local copy of deed: [LICENSE](LICENSE)).


## Authors and Contact
**Nicholas Car**  
*Data Architect*  
Geoscience Australia  
<nicholas.car@ga.gov.au>  
<http://orcid.org/0000-0002-8742-7730>  
