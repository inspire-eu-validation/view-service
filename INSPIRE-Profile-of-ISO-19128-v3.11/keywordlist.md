# Keywordlist

**Purpose**: Keywords shall be mapped to the wms:KeywordList element.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a KeywordList node in each Layer section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.3

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
KeywordList <a name="KeywordList"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:KeywordList
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer
