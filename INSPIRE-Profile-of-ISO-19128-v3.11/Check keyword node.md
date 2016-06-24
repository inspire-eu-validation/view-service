# Check keyword node

**Purpose**: The keywords shall be mapped to the capabilities extension and within an element.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.
* [Schema validation](Schema validation.md)
* No metadata URL is given in test case [MetadataURL reference INSPIRE service metadata](MetadataURL reference INSPIRE service metadata.md)

**Test method**

* Check if there are a [Keyword](#Keyword) node and a [MandatoryKeyword](#MandatoryKeyword) node in the ExtendedCapabilities section
* Check that there exists at least one [MandatoryKeyword](#MandatoryKeyword) element containing one of the keywords listed in [IR MD](README.md#ref_IR_MD), Part D, 4.Classification of Spatial data Services (the lowerCamelCase terms in parenthesis).


**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.7

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Keyword <a name="Keyword"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:Keyword
MandatoryKeyword <a name="MandatoryKeyword"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MandatoryKeyword
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities
