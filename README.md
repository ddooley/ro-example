# ro-example
An example ontology model involving the relation ontology and diabetes.

Use this OntoFox file fetch to refresh the general_import.owl file:

curl -s -F file=@general_ontofox.txt -o general_import.owl http://ontofox.hegroup.org/service.php

Note that Mondo imports "Disease has basis in feature", but marks it as transitive, but this causes reasoning error in conjunction with RO "phenotype of" which is functional.
