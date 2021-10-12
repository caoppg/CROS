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

## Running the tests

Some input data sets are in the "data" folder under the project root dictionary. They can be passed to the command line arguments for running the software. For example, to run on the SECOM data set with support value of 0.853653: -p -if D:\XX\XX\XX\KSPMI-master\data\SECOM.csv -of D:\XX\XX\XX\KSPMI-master\result.txt -m 0.853653.

The [SECOM data set](https://archive.ics.uci.edu/ml/datasets/SECOM) contains measurements of features of semi-conductor productions within a semi-conductor manufacturing process. In the SECOM data set, 1567 recordings and 590 attributes are collected, with each recording being characterized by a time stamp referring to the time that the data is recorded. Each recording is also associated with a label, which is either 1 or -1. The label of every recording explains the correctness of the event, with -1 corresponding to a non-failure event, and 1 refers to a failure. Timestamps are associated with all the records indicating the moment of each specific test point. In total, 104 pieces of records represent the failures of production. The data is stored in a raw text file, within which each line represents an individual example of recording with its timestamp. The features are separated by spaces.

## GUIs
### The frequent chronicle mining GUI
In the frequent chronicle mining interface, a set of extracted failure chronicles are displayed in the table within the figure below. There are three attributes associated with each failure chronicle: support, accuracy, and coverage.

![Alt text](https://github.com/caoppg/KSPMI/blob/master/Screenshots/chroniclemininginterface.PNG?raw=true "The frequent chronicle mining GUI")

### The SWRL rules transformation and rule pruning GUI
After the chronicle mining step, the extracted failure chronicles are transformed into a set of SWRL rules. The SWRL rules transformation and rule pruning GUI allows users to visualize the transformed rules and to select the best-quality rules by using a multi-objective optimization approach. Algorithm used for rule quality optimization: Fast Non-dominated Sorting, introduced in the paper [Non-dominated sorting procedure for pareto dominance ranking on multicore cpu and/or gpu](https://link.springer.com/article/10.1007/s10898-016-0468-7).

![Alt text](https://github.com/caoppg/KSPMI/blob/master/Screenshots/rulegenerationinterface.PNG?raw=true "The SWRL rules transformation and rule pruning GUI")

### The experience capitalization GUI
After obtaining a set of best-quality rules, the experience capitalization phase aims to take as input to the program. The goal of integrating expert rules into the system is to improve the overall fitness of the whole rule base. To enable this step, an experience capitalization GUI is developed to allow users to interact with the expert rule base. Also, the system detects possible issues that may occur during this integration process, such as rule redundancy, conflict, and subsumption.

![Alt text](https://github.com/caoppg/KSPMI/blob/master/Screenshots/ExperienceCapGUI.PNG?raw=true "The experience capitalization GUI")

### The ontology reasoning and failure prediction GUI
Failure prediction is achieved by using the [Drools rule engine](https://www.drools.org/) to perform ontology reasoning on the data that is populated in the domain ontologies. After prediction, a SQWRL query is created to retrieve the prediction results. The SQWRL language takes an antecedent of a SWRL rule and effectively treats it as a pattern specification for a query. To extract the results, a SQWRL query replaces a rule consequent with a retrieval specification.

![Alt text](https://github.com/caoppg/KSPMI/blob/master/Screenshots/predictwith8.PNG?raw=true "The ontology reasoning and failure prediction GUI")

## Demonstration video
A demonstration video of the software can be found at [this link](https://github.com/caoppg/KSPMI/blob/ec82e2143eed7f78ece43ec7ac01fcdb67fa6a22/KSPMI%20demo%20video.mp4).

## Built with

* [Maven](https://maven.apache.org/) - Dependency Management
* [Protégé](https://protege.stanford.edu/) - An ontology editor and framework for building intelligent systems
* [The OWL API](http://owlapi.sourceforge.net/) - An API for OWL 2 and an efficient in-memory reference implementation.
* [The SWRL API](https://github.com/protegeproject/swrlapi) - A Java API for working with the OWL-based SWRL rule and SQWRL query languages.
* [The SQWRL API](https://github.com/protegeproject/swrlapi/wiki/SQWRL) - A SWRL-based query language providing SQL-like operators for extracting information from OWL ontologies.
* [SPMF](https://www.philippe-fournier-viger.com/spmf/index.php?link=download.php) - A Java Open-Source Data Mining Library.
* [Weka](https://www.cs.waikato.ac.nz/ml/weka/) - An open source machine learning software.

## Author

* **Qiushi Cao** 
* Email: qiushi.cao09@gmail.com

## License
This project is licensed under the MIT License - see the [License.md](License) file for details

## Acknowledgments
This work has received funding from INTERREG Upper Rhine (European Regional Development Fund) and the
Ministries for Research of Baden-Württemberg, Rheinland-Pfalz (Germany) and from the Grand Est French Region
in the framework of the Science Offensive Upper Rhine HALFBACK project.
