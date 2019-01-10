# Layer Geographic Bounding Box

**Purpose**: Test that the boundingbox of each layer is mapped to the BoundingBox element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Layer](#layer) element:

    * Check that no [BoundingBox](#BoundingBox) elements in the layer refer to the same CRS.

  * For each named [Layer](#layer) element:

    * Check that at least one [BoundingBox](#BoundingBox) element exists in the layer itself or it is inherited from parent layers.

    * For each [BoundingBox](#BoundingBox) in the layer,

      * Check that the attribute 'CRS' of [BoundingBox](#BoundingBox) is defined in a [CRS](#crs) element of the layer itself or in a parent layer.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.4, Requirement 36

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more for each named layer stated explicitly or inherited from a parent Layer.

A Layer that contains a Named child element is a 'named Layer'.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
BoundingBox <a name="BoundingBox"></a> | wms:Capability/*/wms:Layer/wms:BoundingBox
CRS <a name="crs"></a> | wms:Capability/*/wms:Layer/wms:CRS
