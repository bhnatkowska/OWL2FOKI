# OWL2FOKI
This project contains a jar file (java 1.8) which translates an OWL2 ontology into FOKI meta-model and reverse to OWL to check completeness and correctness of translation.
The elements not translated include:
- annotations (global, local)
- assertons
- some data properties specifics

To run the tool write: 
   java -jar FOKI.jar input_ontology_path output_ontology_path, e.g.
   java -jar FOKI.jar shop.owl shop_FOKI.owl

The tool will read the input ontology (here: shop.owl) and write the result of its translation to FOKI and reverse (OWL2 --> FOKI --> OWL2) under the output_ontology_path using the functional syntax.
The tool will write the input ontology without annotations to the test.owl file (in the current directory) for comparison. 

Additionally, the project contains the results of tests undertaken for the tool:
- ontology_test_WA.owl - contains the testing ontology without annotations written in functional syntax
- ontology_FOKI.owl - contains the result of translation (OWL2 --> FOKI --> OWL2)
