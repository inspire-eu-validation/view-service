# Layer Geographic Bounding Box

**Purpose**: Test that the boundingbox of each layer is mapped to the BoundingBox element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Layer element:

    * For each [CRS](#crs) listed in the [Layer](#layer), 
    
      * Check that there is a [BoundingBox](#BoundingBox) element in the same Layer section with the corresponding "CRS" attribute.


**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.4, Requirement 36

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
BoundingBox <a name="BoundingBox"></a> | wms:Capability/*/wms:Layer/wms:BoundingBox
CRS <a name="crs"></a> | wms:Capability/wms:Layer/wms:CRS
Layer <a name="layer"></a> | wms:Capability/wms:Layer
