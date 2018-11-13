# Layer Title

**Purpose**: Test that each layer element contains a Title element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Layer element:

    * Check that it contains a [Title](#title) element and it is a non-empty value.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.1, Requirement 33

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 for each layer element.

Title element shall be subject to multilingualism, therefore, translations shall appear in each mono-lingual capabilities localised documents.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | wms:Capability/*/wms:Layer/wms:Title
