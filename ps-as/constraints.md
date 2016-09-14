# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* Sites must use [designations](#designations) from an appropriate designation scheme, and the designation code value must agree with the designation scheme. Verify that all (pre-defined) designation values are consistent with the designation scheme.

    ```
    inv: self.designationScheme = DesignationSchemeValue::natura2000 implies self.designation.oclIsKindOf(DesignationValueNatura2000) and
    self.designationScheme = DesignationSchemeValue::emeraldNetwork implies self.designation.oclIsKindOf(DesignationValueEmeraldNetwork) and
    self.designationScheme = DesignationSchemeValue::ramsar implies self.designation.oclIsKindOf(DesignationValueRamsar) and
    self.designationScheme = DesignationSchemeValue::UNESCOWorldHeritage implies self.designation.oclIsKindOf(DesignationValueUNESCOWorldHeritage) and
    self.designationScheme = DesignationSchemeValue::IUCN implies self.designation.oclIsKindOf(DesignationValueIUCN) and
    self.designationScheme = DesignationSchemeValue::UNESCOManAndBiosphereProgramme implies self.designation.oclIsKindOf(DesignationValueUNESCOManAndBiosphereProgramme) and self.designationScheme = DesignationSchemeValue::nationalMonumentsRecord implies self.designation.oclIsKindOf(DesignationValueNationalMonumentsRecord)
    ```

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-n-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-PS](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-n-as/README#ref_TG_DS_PS)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-ps/3.2/ps-p-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
designation (v3) <a name="designation3"></a> |  //schema-element(ps3:ProtectedSite)/ps3:siteDesignation/\*[ps3:designationScheme=('IUCNDesignationValue', 'NationalMonumentsRecordDesignationValue', 'Natura2000DesignationValue', 'RamsarDesignationValue', 'UNESCOManAndBiosphereProgrammeDesignationValue', 'UNESCOWorldHeritageDesignationValue')]/ps3:designation/text()
designation (v4) <a name="designation4"></a> |  //schema-element(ps:ProtectedSite)/ps:siteDesignation/\*[fn:substring-after(ps:designationScheme,'http://inspire.ec.europa.eu/codelist/DesignationSchemeValue/')=('IUCNDesignationValue', 'NationalMonumentsRecordDesignationValue', 'Natura2000DesignationValue', 'RamsarDesignationValue', 'UNESCOManAndBiosphereProgrammeDesignationValue', 'UNESCOWorldHeritageDesignationValue')]/ps:designation/@xlink:href

