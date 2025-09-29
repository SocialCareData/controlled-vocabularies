# controlled-vocabularies
Controlled Vocabularies required to implement the DSSC specifications


### Where do we need controlled vocabularies?
#### Person Spec
* identifier system -- this would have to be a set of namespaces for identifiers? I guess not a controlled vocab, because it expects URI. but lots of identifier systems won't have URIs, so will have to define our own like [FHIR does for a lot of identifier namespaces](https://terminology.hl7.org/identifiers.html)
* name.use -- we just copied FHIR's coding, but can expand
* birth date accuracy indicator -- just explain what each letter means I guess
* gender
* sex


#### Placement spec
* planned vs emergency, although that's meant to be a boolean so idk maybe the spec needs changing there
* daily / few times a week / whatever -- just need codes for these
* communication needs
* provision recommendations
* risks

#### API catalogue
* types

#### request/response templates
* error codes