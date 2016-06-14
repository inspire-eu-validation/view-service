# A.31.IR36.layer.bbox.node

**Purpose**: This Layer metadata element shall be mapped to the wms:BoundingBox element. The minimum bounding rectangle of the area covered by the Layer in all supported CRS shall be given.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* For each [CRS](#wmsCRS) that is listed for a specific [Layer](#Layer), check if there is a [BoundingBox](#BoundingBox) node in the same [Layer](#Layer) section with a corresponding attribute [@CRS](#CRS).

**Reference(s)**:
* IR Annex III, Part A, Chapter 2.2.4
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.4

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer
CRS <a name="wmsCRS"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:CRS
BoundingBox <a name="BoundingBox"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/BoundingBox
@CRS <a name="CRS"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/BoundingBox[@CRS]
