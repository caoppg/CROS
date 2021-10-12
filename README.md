# CROS
The ontology files for the paper "A core reference ontology for steelmaking process knowledge modelling and information management". This work is funded by the EPSRC project SUSTAIN (https://www.sustainsteel.ac.uk/)

## Getting started

To open the ontology, the following steps should be followed:

* Download .owl files.
* Save the .owl files in a same folder.
* Download an ontology editor software, such as [Protégé] (https://protege.stanford.edu/).
* Use Protégé to open the CROS.owl file.


### Ontology main classes:

The following figure shows the ontology main classes:

![Alt text](https://github.com/caoppg/CROS/blob/main/Figs/OntoMainClasses.png)

### Ontology main properties:

The following figure shows the ontology main object and data properties:

![Alt text](https://github.com/caoppg/CROS/blob/main/Figs/Ontorelationships.png)

## Case study

The ontology is evaluated and tested on a real-world case study. This case study is about a condition-based maintenance task performed on a cold rolling process at a Tata Steel plant in the UK. The aim of the case study is to evaluate the functionality and usefulness of CROS under real-world scenarios.  We focus on the knowledge reuse and information man-agement perspectives within this condition-based maintenance task.  The obtained results prove that CROS and its related ontological modelling toolsare easy to use for knowledge embedding, data access, and information re-trieval within the steelmaking domain. The remainder of this section gives adetailed description of our experimental set-up, data collection, and ontology-based predictive maintenance process.

A high-level visualisation of roll management system for cold rolling mills:
![Alt text](https://github.com/caoppg/CROS/blob/main/Figs/ColdRollingPic.png)

### Ontology-based data access using CROS
The predictive and condition-based maintenance task of Port Talbot cold rolling mills is carried out using OBDA techniques. In this work, we use the Virtual Knowledge Graph System [Ontop](https://ontop-vkg.org). Ontop can map domain ontologies to arbitrary relational databases using R2RML, Direct Mapping, and its own mapping language. The advantage of Ontop is its adoption of Virtual Knowledge Graphs. As the graphs (ontologies) are kept virtual, it avoids the manipulation of relational databases, which is normally considered as work-intensive and expensive. In this way, Ontop provides convenient access to databases and eases the task of data integration. 

A tutorial using Ontop can be found at: https://ontop-vkg.org/tutorial/.

## Built with
* [Protégé](https://protege.stanford.edu/) - An ontology editor and framework for building intelligent systems
* [The OWL API](http://owlapi.sourceforge.net/) - An API for OWL 2 and an efficient in-memory reference implementation
* [The SWRL API](https://github.com/protegeproject/swrlapi) - A Java API for working with the OWL-based SWRL rule and SQWRL query languages
* [Ontop](https://ontop-vkg.org/tutorial/) - A Virtual Knowledge Graph System
* [SPARQL](https://www.w3.org/TR/rdf-sparql-query/) - A semantic query language for databases

## Author

* **Qiushi Cao** 
* Email: qiushi.cao09@gmail.com

## License
This project is licensed under the MIT License - see the [License.md](License) file for details

## Acknowledgments
This work is mainly funded by the Engineering and Physical Sciences Research Council (EPSRC) [grant number EPSRC EP/S018107/1].

