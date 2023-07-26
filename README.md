# xai-non-entailments
Explaining EL Non-entailments via Subtree Isomorphisms

This is the repository for the "Explaining EL Non-entailments via Subtree Isomorphisms" journal paper, submitted at the Journal of Web Semantics.

This repository contains the files/folders:

1) functions.py - contains functions used in the code, separated in a distinct script

2) pathfinder.py - implementation of search algorithm for paths in rooted trees

3) isomorphisms.py - implementation of (i) compute isomorphisms, (ii) construct polynomials, (iii) equalize polynomials, and (iv) construct hypotheses, (ii, iii, and iv are directly implemented in i)

4) main.py - implementation of class DescriptionTrees and main simulation environment

5) Simulations_test - folder containing simulation results (ontologies + DataFrame of results) for parameters [a, b] = [1, 10], [c, d] = [1, 10]. This folder was created to test whether the code works.

Libraries used:

1) owlready2 - https://owlready2.readthedocs.io/en/latest/intro.html

	Owlready2 is a package for manipulating OWL 2.0 ontologies in Python. It can load, modify, save ontologies, and it supports reasoning via HermiT (included). Owlready allows a transparent access to 	OWL ontologies.

In order for the HermiT reasoner to be used with the package owlready2, you need to install JDK20 (https://www.oracle.com/java/technologies/downloads/) and add it in the systems path.

All additional Python libraries can be seen imported in each .py script in the repository. In order for the code to run, all libraries must be installed. We recommend using Anaconda (https://www.anaconda.com/download) as a base for using Spyder (the IDE in which the implementation is). Most of the libraries are already installed there. To install new libraries add command pip install 'library_name' in the Console of Spyder.

Protege:

The experiments are performed w.r.t. ontologies, saved as .owl files. To directly read the generated ontologies, please download Protege (https://protege.stanford.edu/).

Running the simulations:

To run the experiments open the main.py script and run it. Provided that all the necessary libraries are installed, the algorithm will first ask for a path of the folder in which you wish to save the results. Please provide the complete path of this folder and click Enter. After, the algorithm will perform the experiments and save the ontologies and results in that folder. 

Each ontology can be accessed to see which axioms have been added to it. The .csv and .html files represent the statistics of the simulations. To extract the statistics in the paper, run the results.py script. Please input the complete path (including the file_name.csv) so that the results.py script can read the simulation results. In addition, the script result.py provides a scatterplot of the reults (mean of max repetition of common edge labels) vs (# H - number of hypotheses), as in the journal paper.
