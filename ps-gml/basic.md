# Basic test

**Version**: 1

**Purpose**: Verify that the spatial data set contains at least one Protected Site feature.

**Prerequisites**

**Test method**

* Check that the set of [features](#features) in the spatial data set is not empty. Otherwise report [noFeature](#noFeature)

**Reference(s)**: 

* [TG DS-PS](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-gml/README#ref_TG_DS_PS) 5.3

**Test type**: Automated

**Notes**

There is no requirement that we could reference in the Technical Guidelines, but such a requirement is clearly missing for any data set with psdrographic features. Maybe such a requirement should be added in the future revision?

## Messages

Identifier  |  Message text (parameters start with '$')
----------- | -------------------------------------------------------------------------
noFeature <a name="noFeature"/>  |  	The XML documents representing the spatial data set do not contain a feature of any of the spatial object types in the 'Protected Sites Simple' application schemas. Therefore, the spatial data set cannot conform to this conformance class. If you have expected to find spatial objects from the application schema in the data set, please consult the statistics information to see the spatial object types that have been found.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-gml/README#namespaces).

Abbreviation                                          |  XPath expression
----------------------------------------------------- | ------------------------------------------------------------------
features <a name="features"></a>   |  //schema-element(ps:ProtectedSite)