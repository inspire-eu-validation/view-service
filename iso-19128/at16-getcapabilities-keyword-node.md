# Keyword Node

**Purpose**: Test that at least one keyword from the "Classification of Spatial data Services" is provided.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if at least one [Keyword](#keyword) element with a keyword from the "Classification of Spatial data Services" (Part D.4) is provided.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.7, Requirement 16
* [INS MD](./README.md#ref_INS_MD), Classification of Spatial data Services, Part D.4

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Keyword <a name="keyword"></a> | wms:Service/*/wms:Keyword