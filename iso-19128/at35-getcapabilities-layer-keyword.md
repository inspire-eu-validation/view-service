# Layer Keyword

**Purpose**: Test that the additional keywords describing the layer are mapped to the KeywordList element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Layer](#layer) element:

    * Check that zero or one [KeywordList](#KeywordList) element exists. If [Keyword](#Keyword) elements exists in [KeywordList](#KeywordList) node,

        * Check [Keyword](#Keyword) is not empty.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.3, Requirement 35

**Test type**: Automated

**Notes**

The multiplicity of [KeywordList](#KeywordList) is 0 or 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
KeywordList <a name="KeywordList"></a> | wms:Capability/*/wms:Layer/wms:KeywordList
Keyword <a name="Keyword"></a> | wms:Capability/*/wms:Layer/wms:KeywordList/wms:Keyword

