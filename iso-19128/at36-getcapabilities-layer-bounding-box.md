# Layer Geographic Bounding Box

**Purpose**: Test that the boundingbox of each layer is mapped to the BoundingBox element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Layer element:

    * Check if the minimum bounding rectagle of the area covered by the layer is mapped to the [BoundingBox](#BoundingBox) element in all supported CRS.


**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.4, Requirement 36

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
BoundingBox <a name="BoundingBox"></a> | wms:Capability/*/wms:Layer/wms:BoundingBox
