# Conformance class: Information accessibility, Protected Sites (DRAFT)

Conformance class for the requirements related to the accessibility of referenced information, for example, information stored in registries (code lists, coordinate reference systems).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schema for Protected Sites".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Protected Sites](http://inspire.ec.europa.eu/id/ats/data-ps/3.2).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-ia/README#ref_TG_DS_tmpl) | [Information accessibility](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/information-accessibility) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-PS](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-ia/README#ref_TG_DS_PS) | [GML application schema, Protected Sites - Network](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-gml) | INSPIRE spatial data set encoded in GML, Protected Sites features | n/a |
 
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

| Identifier                                                        | Status   | Test case in [TG DS-PS](#ref_TG_DS_PS)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code lists](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-ia/code-list)  | ready for review  | A.6.1 |
| [Feature references](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/hy-ps/features)  | ready for review  | A.1.4 |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gml            | http://www.opengis.net/gml/3.2
ps3            | urn:x-inspire:specification:gmlas:ProtectedSites:3.0
ps             | http://inspire.ec.europa.eu/schemas/ps/4.0

The following variables are used to refer to the corresponding Xpath expressions in all test descriptions:

Variable       | Value
-------------- | -------------------------------------------------
$features      |  //schema-element(ps-n:HydroNode) \| //schema-element(ps-n:WatercourseLink) \| //schema-element(ps-n:WatercourseLinkSequence) \| //schema-element(ps-n:WatercourseSeparatedCrossing) \| //schema-element(ps-p:Watercourse) \| //schema-element(ps-p:StandingWater) \| //schema-element(ps-p:Wetland) \| //schema-element(ps-p:GlacierSnowfield) \| //schema-element(ps-p:Shore) \| //schema-element(ps-p:DrainageBasin) \| //schema-element(ps-p:RiverBasin) \| //schema-element(ps-p:LandWaterBoundary) \| //schema-element(ps-p:Embankment) \| //schema-element(ps-p:Ford) \| //schema-element(ps-p:Lock) \| //schema-element(ps-p:Sluice) \| //schema-element(ps-p:DamOrWeir) \| //schema-element(ps-p:ShorelineConstruction) \| //schema-element(ps-p:Crossing) \| //schema-element(ps-p:SpringOrSeep) \| //schema-element(ps-p:VanishingPoint) \| //schema-element(ps-p:Rapids) \| //schema-element(ps-p:Falls)
