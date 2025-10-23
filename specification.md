# Controlled Vocabularies

## `Name.use`
A person can have more than one name on their record. The Name object, therefore, requires a Name.use data point, a categorical variable encoded by Name.use. We reuse [FHIR's NameUse binding](http://hl7.org/fhir/codesystem-name-use.html).

Used in:
* Person Data Standard (Identification)

Inherits from:
* [FHIR NameUse](http://hl7.org/fhir/codesystem-name-use.html)

|Code|Display|Definition|
|:---|:------|:---------|
|`usual`|Usual|Known as/conventional/the name you normally use.|
|`official`|Official|The formal name as registered in an official (government) registry, but which name might not be commonly used. May be called "legal name".|
|`temp`|Temp|A temporary name. This may be used for temporary names assigned at birth or in emergency situations.|
|`nickname`|Nickname|A name that is used to address the person in an informal manner, but is not part of their formal or usual name.|
|`anonymous`|Anonymous|Anonymous assigned name, alias, or pseudonym (used to protect a person's identity for privacy reasons)|
|`old`|Old|A name that is no longer in use (or was never correct, but retained for records)|
|`maiden`|Maiden|A name used prior to changing name because of marriage. This name use is for use by applications that collect and store names that were used prior to a marriage. Marriage naming customs vary greatly around the world, and are constantly changing. This term is not gender specific. The use of this term does not imply any particular history for a person's name.|

<a href="https://github.com/SocialCareData/controlled-vocabularies/issues/new?template=content_issue.yml&amp;title=Issue+regarding+Name.use" class="web-button" target="_blank">Raise an issue about Name.use</a>

## `DateOfBirth.accuracyIndicator`
Birth dates may be unknown, estimated, or accurate, across years, months, or days. We therefore require a Birth Date Accuracy Indicator, which conforms to date-accuracy-indicator and is a triple of letters that aligns with ISO 8601 date format (Y-M-D, so eg. AEU for accurate year, estimated month, unknown day).

`DateOfBirth.accuracyIndicator` has cardinality 0,1. If it is not present, we assume AAA. 

Used in:
* Person Data Standard (Identification)

Aligns with:
* [FHIR AU extension](https://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-date-accuracy-indicator.html)

|Code|Display|Definition|
|:---|:------|:---------|
|`A`|Accurate|Known, confirmed element of the date. Not necessarily confirmed with certified evidence (such as a birth or death certificate).|
|`E`|Estimated|An estimated element of the date, with the estimate provided by a professional or the person themselves.|
|`U`|Unknown|Entirely unknown and unestimable element of the date. |
|`X`|Expected|For use with pre-natal persons with expected dates of birth|

<a href="https://github.com/SocialCareData/controlled-vocabularies/issues/new?template=content_issue.yml&amp;title=Issue+regarding+DateOfBirth.accuracyIndicator" class="web-button" target="_blank">Raise an issue about DateOfBirth.accuracyIndicator</a>

## `Gender`
(TODO: add notes here) 

Used in:
* Person Data Standard (Identification)

Aligns with:
* [NHS Person Stated Gender Code](https://archive.datadictionary.nhs.uk/DD%20Release%20May%202024/attributes/person_stated_gender_code.html)

|Code|Display|Definition|
|:---|:------|:---------|
|`1`|Male|
|`2`|Female|
|`9`|Indeterminate|Unable to be classified as either male or female|

<a href="https://github.com/SocialCareData/controlled-vocabularies/issues/new?template=content_issue.yml&amp;title=Issue+regarding+Gender" class="web-button" target="_blank">Raise an issue about Gender</a>

## `Sex`
(TODO: add notes here) 

Used in:
* Person Data Standard (Identification)

Aligns with:
* [NHS Person Phenotypic Sex Classification](https://archive.datadictionary.nhs.uk/DD%20Release%20May%202024/attributes/person_phenotypic_sex_classification.html)

|Code|Display|Definition|
|:---|:------|:---------|
|`1`|Male|
|`2`|Female|
|`9`|Indeterminate|Unable to be classified as either male or female|

<a href="https://github.com/SocialCareData/controlled-vocabularies/issues/new?template=content_issue.yml&amp;title=Issue+regarding+Sex" class="web-button" target="_blank">Raise an issue about Sex</a>