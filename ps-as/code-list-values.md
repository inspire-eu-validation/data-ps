# Code list values

**Version**: 1

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II of the regulation. To pass this tests that any instance of an attribute

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.

Otherwise report [disallowedCodeListValue](#disallowedCodeListValue).

In the Protected Sites Simple application schema, **no** properties can be tested in an automated way as both DesignationValue and DesignationSchemeValue have extensibility 'open'.

Inspect the code list valued property elements 

* [designation (v3)](#designation3) and [designationScheme (v3)](#designationScheme3) for data using the version 3 GML application schema,
* [designation (v4)](#designation4) and [designationScheme (v4)](#designationScheme4) for data using the version 4 GML application schema. 

If a value is not one of the values listed in the data specification, review the code list definition to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements. This is a manual test.
  
**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Manual

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-p-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
designation (v3) <a name="designation3"></a> |  //schema-element(ps3:ProtectedSite)/ps3:siteDesignation/\*/ps3:designation/text()
designation (v4) <a name="designation4"></a> |  //schema-element(ps:ProtectedSite)/ps:siteDesignation/\*/ps:designation/@xlink:href
designationScheme (v3) <a name="designationScheme3"></a> |  //schema-element(ps3:ProtectedSite)/ps3:siteDesignation/\*/ps3:designationScheme/text()
designationScheme (v4) <a name="designationScheme4"></a> |  //schema-element(ps:ProtectedSite)/ps:siteDesignation/\*/ps:designationScheme/@xlink:href