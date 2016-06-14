# A.13.IR18.keywords.node

**Purpose**: The keywords shall be mapped to the capabilities extension and within an element.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.
* [A.03.IR05.schema.validation](A.03.IR05.schema.validation.md)

**Test method**

* Check if there are a Keyword node and a MandatoryKeyword node in the ExtendedCapabilities section
* Check that there exists at least one [MandatoryKeyword element](#ext-mandatory-keyword) containing one of the keywords listed in [IR MD](README.md#ref_IR_MD), Part D, 4.Classification of Spatial data Services (the lowerCamelCase terms in parenthesis).


**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.7

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Keyword <a name="Keyword"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:Keyword
MandatoryKeyword <a name="MandatoryKeyword"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:MandatoryKeyword
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities
