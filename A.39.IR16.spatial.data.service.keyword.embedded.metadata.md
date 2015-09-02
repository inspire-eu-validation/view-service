# A.39.IR16.spatial.data.service.keyword.embedded.metadata

**Purpose**: The INSPIRE Metadata Regulation [INS MD] mandates that in the case of spatial data services at least
one keyword from the "Classification of Spatial data Services" (Part D.4 from INS MD] shall be provided.

**Prerequisites**

* [A.03.IR05.schema.validation](A.03.IR05.schema.validation.md)
* [A.05.IR07.extended.capabilities.elements.node](A.05.IR07.extended.capabilities.elements.node.md)
* [A.13.IR18.keywords.node](A.13.IR18.keywords.node.md)

**Test method**

Check that there exists at least one [MandatoryKeyword element](#ext-mandatory-keyword) containing one of the keywords listed in [IR MD](README.md#ref_IR_MD), Part D, 4.Classification of Spatial data Services (the lowerCamelCase terms in parenthesis).

**Reference(s)**

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
MandatoryKeyword <a name="ext-mandatory-keyword"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities[1]/inspire_common:MandatoryKeyword
