# Layer Metadata

**Purpose**: Test that each layer is uniquely identified by a harmonished name.

**Prerequisites**

**Test method**

The Unique Resource Identifier and Name INSPIRE metadata elements are mapped to the Identifier OGC WMTS standard element.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if an [Identifier](#identifier) element is given and it is a non-empty free text.

      * [Identifier](#identifier)  element value must match with one of the harmonised layer names given in [TG VS](./README.md#ref_TG_VS) or it's amendments.

  * Check if each identifier value is unique for each of the layers included in the GetCapabilities response.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4, Requirement 84

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 for each layer.

The mapping between of the rest INSPIRE layer metadata elements and OGC WMTS elements is implemented in the Abstract Tests from [at85](./at85-getcapabilities-layer-title.md) to [at91](./at91-getcapabilities-layer-legend-url.md).

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Identifier <a name="identifier"></a> | Contents/Layer/ows:Identifier