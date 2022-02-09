# wikidata-queries

This repository contains queries to Wikidata that summarize the Laboratory of Systems Pharmacology.

- [Organization Visualization](https://query.wikidata.org/embed.html#%23%20tool%3A%20scholia%0A%23defaultView%3AGraph%0A%0ASELECT%0A%20%20%3Fsubject%20%3FsubjectLabel%20%3Fimage1%20%3Frgb%20%3FedgeLabel%0A%20%20%3Fobject%20%3FobjectLabel%20%3Fimage2%0AWHERE%20%7B%0A%20%20%7B%0A%20%20%20%20SELECT%0A%20%20%20%20%20%20(%3Flab%20as%20%3Fsubject)%20(%3FlabLabel%20as%20%3FsubjectLabel)%20%3Fimage1%0A%20%20%20%20%20%20%3Frgb%20%3FedgeLabel%0A%20%20%20%20%20%20(%3Fperson%20as%20%3Fobject)%20(%3FpersonLabel%20as%20%3FobjectLabel)%20%3Fimage2%0A%20%20%20%20WHERE%20%7B%0A%20%20%20%20%20%20%3Flab%20wdt%3AP361%20wd%3AQ107380113%20.%0A%20%20%20%20%20%20%3Fperson%20wdt%3AP1416%20%3Flab%20.%0A%20%20%20%20%20%20OPTIONAL%20%7B%20%3Flab%20wdt%3AP18%20%3Fimage1%20%7D%0A%20%20%20%20%20%20OPTIONAL%20%7B%20%3Fperson%20wdt%3AP18%20%3Fimage2%20%7D%0A%20%20%20%20%20%20BIND(%22FF00FF%22%20AS%20%3Frgb)%20.%0A%20%20%20%20%20%20BIND(%22affiliate%22%20AS%20%3FedgeLabel)%20.%0A%20%20%20%20%7D%0A%20%20%7D%20%20%0A%20%20UNION%0A%20%20%7B%0A%20%20%20%20SELECT%0A%20%20%20%20%20%20(%3Flab%20as%20%3Fsubject)%20(%3FlabLabel%20as%20%3FsubjectLabel)%20%3Fimage1%0A%20%20%20%20%20%20%3Frgb%20%3FedgeLabel%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%0A%20%20%20%20%20%20(%3Fmanager%20as%20%3Fobject)%20(%3FmanagerLabel%20as%20%3FobjectLabel)%20%3Fimage2%0A%20%20%20%20WHERE%20%7B%0A%20%20%20%20%20%20%3Flab%20wdt%3AP361%20wd%3AQ107380113%20.%0A%20%20%20%20%20%20%3Flab%20wdt%3AP1037%20%3Fmanager%20.%0A%20%20%20%20%20%20OPTIONAL%20%7B%20%3Flab%20wdt%3AP18%20%3Fimage1%20%7D%0A%20%20%20%20%20%20OPTIONAL%20%7B%20%3Fmanager%20wdt%3AP18%20%3Fimage2%20%7D%0A%20%20%20%20%20%20BIND(%22FF00FF%22%20AS%20%3Frgb)%20.%0A%20%20%20%20%20%20BIND(%22directed%20by%22%20AS%20%3FedgeLabel)%20.%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20UNION%0A%20%20%7B%0A%20%20%20%20SELECT%0A%20%20%20%20%20%20(%3Flab1%20as%20%3Fsubject)%20(%3Flab1Label%20as%20%3FsubjectLabel)%20%3Fimage1%0A%20%20%20%20%20%20%3Frgb%20%3FedgeLabel%0A%20%20%20%20%20%20(%3Flab2%20as%20%3Fobject)%20(%3Flab2Label%20as%20%3FobjectLabel)%20%3Fimage2%0A%20%20%20%20WHERE%20%7B%0A%20%20%20%20%20%20%3Flab1%20wdt%3AP361%20wd%3AQ107380113%20.%0A%20%20%20%20%20%20%3Flab2%20wdt%3AP361%20wd%3AQ107380113%20.%0A%20%20%20%20%20%20%3Flab1%20wdt%3AP361%20%3Flab2%20.%0A%20%20%20%20%20%20OPTIONAL%20%7B%20%3Flab1%20wdt%3AP18%20%3Fimage1%20%7D%0A%20%20%20%20%20%20OPTIONAL%20%7B%20%3Flab2%20wdt%3AP18%20%3Fimage2%20%7D%0A%20%20%20%20%20%20BIND(%22FF00FF%22%20AS%20%3Frgb)%20.%0A%20%20%20%20%20%20BIND(%22part%20of%22%20AS%20%3FedgeLabel)%20.%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20UNION%20%0A%20%20%7B%0A%20%20%20%20SELECT%0A%20%20%20%20%20%20(%3Fauthor1%20as%20%3Fsubject)%20(%3Fauthor1Label%20as%20%3FsubjectLabel)%20%3Fimage1%0A%20%20%20%20%20%20%3Frgb%20%3FedgeLabel%0A%20%20%20%20%20%20(%3Fauthor2%20as%20%3Fobject)%20(%3Fauthor2Label%20as%20%3FobjectLabel)%20%3Fimage2%0A%20%20%20%20WHERE%20%7B%0A%20%20%20%20%20%20wd%3AQ107380113%20%5Ewdt%3AP361*%20%2F%20%5E(%20wdt%3AP108%20%7C%20wdt%3AP1416%20%7C%20wdt%3AP463%20)%20%3Fauthor1%20%2C%20%3Fauthor2%20.%20%0A%20%20%20%20%20%20%3Fwork%20wdt%3AP50%20%3Fauthor1%20%2C%20%3Fauthor2%20.%0A%0A%20%20%20%20%20%20%23%20Only%20display%20co-authorship%20for%20certain%20types%20of%20documents%0A%20%20%20%20%20%20%23%20Journal%20and%20conference%20articles%2C%20books%2C%20not%20(yet%3F)%20software%0A%20%20%20%20%20%20VALUES%20%3Fpublication_type%20%7B%20wd%3AQ13442814%20wd%3AQ571%20wd%3AQ26973022%20wd%3AQ17928402%20wd%3AQ947859%20wd%3AQ54670950%20%7D%0A%20%20%20%20%20%20FILTER%20EXISTS%20%7B%20%3Fwork%20wdt%3AP31%20%3Fpublication_type%20.%20%7D%0A%0A%20%20%20%20%20%20%23%20No%20self-links.%0A%20%20%20%20%20%20FILTER%20(%3Fauthor1%20!%3D%20%3Fauthor2)%0A%0A%20%20%20%20%20%20%23%20Images%0A%20%20%20%20%20%20OPTIONAL%20%7B%20%3Fauthor1%20wdt%3AP18%20%3Fimage1%20%7D%0A%20%20%20%20%20%20OPTIONAL%20%7B%20%3Fauthor2%20wdt%3AP18%20%3Fimage2%20%7D%0A%0A%20%20%20%20%20%20%23%20Coloring%20of%20the%20nodes%0A%20%20%20%20%20%20BIND(%22FFFFFF%22%20AS%20%3Frgb)%0A%20%20%20%20%20%20BIND(%22coauthored%22%20AS%20%3FedgeLabel)%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%2Cda%2Cde%2Ces%2Cfr%2Cjp%2Csv%2Cru%2Czh%22.%20%7D%0A%7D%0A)

## How to run a query

1. Choose your query
2. Copy/paste the whole file into https://query.wikidata.org/
3. Press the blue play button to see the results

## Glossary

Wikidata can be queried using the [SPARQL Query Language](https://www.w3.org/TR/rdf-sparql-query/), which is like SQL for graph-like databases that store their data in [Resource Description Framework (RDF)](https://www.w3.org/RDF/).
