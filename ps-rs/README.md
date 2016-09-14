# Conformance class: Reference systems, Protected Sites (DRAFT)

Conformance class for the requirements associated with reference systems (spatial and temporal, units of measurement).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schema for Protected Sites".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Protected Sites](http://inspire.ec.europa.eu/id/ats/data-ps/3.2).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-rs/README#ref_TG_DS_tmpl) | [Reference systems](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/reference-systems) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-PS](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-rs/README#ref_TG_DS_PS) | [GML application schema, Protected Sites Simple](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-gml) | INSPIRE spatial data set encoded in GML, Protected Sites features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:
 
* ProtectedSite
 
*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-PS <a name="ref_TG_DS_PS"></a>   | [INSPIRE Data Specification on Protected Sites – Technical Guidelines version 3.2](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_PS_v3.2.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

None, all reference system test cases are covered by the generic [Reference systems](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/reference-systems) tests.

## XML namespace prefixes <a name="namespaces"></a>

n/a