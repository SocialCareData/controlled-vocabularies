# controlled-vocabularies
Where categorical data is required across our data standards, we require a clear definitions of what categories can be chosen for what kinds of data, what each category means, how it is encoded, and more. This repo serves as a central location for this information.


### Where do we need controlled vocabularies?
#### Person Spec
* Identifier.system.URI
    *  A person can have more than one unique identifier. For example, they may be registered as case number 029834 in their local authority's social care management system, but they could also be referenced as patient number 2a309e in the same local authority's welfare provision database. To distinguish what system a described Identifier.value conforms to (in a machine-readable way), we require a value for Identifier.system, which conforms to the data type Identifier.system.URI.
    * This URI should be a namespace the identifier. While this is not strictly categorical data, and does not necessarily require a controlled vocabulary, we note that many identifier systems may not have associated namespace URIs. 
    * We therefore propose defining (a sample) of our own, like [FHIR does for a lot of identifier namespaces](https://terminology.hl7.org/identifiers.html).
* Name.use.type
    * Similarly, a person can have more than one name on their record. The Name object, therefore, requires a Name.use data point, a categorical variable encoded by Name.use.type.
    * This is proposed to reuse FHIR's [NameUse binding](https://build.fhir.org/valueset-name-use.html), where a name can be one of: {usual, official, temp, nickname, anonymous, old, maiden}.
    * We could expand on this terminology if necessary.
* Date-accuracy-indicator
    * Birth dates may be unknown, estimated, or accurate, across years, months, or days. 
    * We therefore require a Birth Date Accuracy Indicator, which conforms to date-accuracy-indicator and is a triple of letters (eg. AEU for accurate year, estimated month, unknown day)
    * This is aligned with HL7 Australia's proposed addition to FHIR (link??), although with Y-M-D order as per ISO 8601
* Gender
    * Note discussion on this subject
    * We're referencing the [NHS Person Stated Gender Code](https://archive.datadictionary.nhs.uk/DD%20Release%20May%202024/data_elements/person_stated_gender_code.html)
* Sex
    * Note discussion on this subject
    * We're referencing the [NHS Person Phenotypic sex](https://archive.datadictionary.nhs.uk/DD%20Release%20May%202024/data_elements/person_phenotypic_sex.html) 


#### Placement spec
* planned vs emergency, although that's meant to be a boolean so idk maybe the spec needs changing there
* daily / few times a week / whatever -- just need codes for these
* communication needs
* provision recommendations
* risks

#### API catalogue
* types

#### request/response templates
* error codes?