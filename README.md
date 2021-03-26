# ro-example
An example ontology model involving the relation ontology and diabetes.

Use this OntoFox file fetch to refresh the general_import.owl file:

curl -s -F file=@general_ontofox.txt -o general_import.owl http://ontofox.hegroup.org/service.php

Use this robot command to get an inferred ontology.  Note, Protege seems to freeze up on displaying 'blood vessel diameter' with hermit reasoner active on the ro-example.owl file and default reasoning options. Hence the ro-inferred.owl file may be a preferred way to explore such content in Protege.

robot reason --input ro-example.owl --reasoner hermit --output ro-inferred.owl --axiom-gerators "SubClass ClassAssertion PropertyAssertion"

Note that using "includeAllAxiomsRecursively" in general_ontofox.txt causes a reasoning error when Mondo imports "Disease has basis in feature", but marks it as transitive, but this causes reasoning error in conjunction with RO "phenotype of" which is functional.
