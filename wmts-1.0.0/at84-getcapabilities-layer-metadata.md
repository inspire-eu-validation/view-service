# Layer Metadata

**Purpose**: Test that each layer is uniquely identified by an harmonished name.

**Prerequisites**

**Test method**

The Unique Resource Identifier and Name INSPIRE metadata elements are mapped to the Identifier OGC WMTS standard element.

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Layer](#layer) element:

    * Check if an [Identifier](#identifier) element is given and it is a non-empty value.

      * [Identifier](#identifier) element value must match with one of the harmonised layer names given in [TG VS](./README.md#ref_TG_VS) or it's amendments.

    * Check if each identifier value is unique for each of the layers included in the GetCapabilities response.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4, Requirement 84

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 for each layer.

The mapping between the rest of INSPIRE layer metadata elements and OGC WMTS elements is implemented in the Abstract Tests from [at85](./at85-getcapabilities-layer-title.md) to [at91](./at91-getcapabilities-layer-legend-url.md).

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | Contents/Layer
Identifier <a name="identifier"></a> | Contents/Layer/ows:Identifier