# Layer Keyword

**Purpose**: Test that the additional keywords describing the layer are mapped to the KeywordList element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Layer element:

    * Check that [Keyword](#Keyword) elements are mapped to the [KeywordList](#KeywordList) element.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.3, Requirement 35

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
KeywordList <a name="KeywordList"></a> | wms:Capability/*/wms:Layer/wms:KeywordList
Keyword <a name="Keyword"></a> | wms:Capability/*/wms:Layer/wms:KeywordList/wms:Keyword

