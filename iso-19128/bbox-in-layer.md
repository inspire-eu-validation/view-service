# Bounding box in layer

**Purpose**: This Layer metadata element shall be mapped to the wms:BoundingBox element. The minimum bounding rectangle of the area covered by the Layer in all supported CRS shall be given.

**Prerequisites**

* [Schema validation](./schema-validation.md)

**Test method**

* For each [CRS](#wmsCRS) that is listed for a specific [Layer](#Layer), check if there is a [BoundingBox](#BoundingBox) node in the same [Layer](#Layer) section with a corresponding attribute [@CRS](#CRS).

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.4, Requirement 36 

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a> | ./wms:Capability/wms:Layer
CRS <a name="wmsCRS"></a> | ./wms:Capability/wms:Layer/wms:CRS
BoundingBox <a name="BoundingBox"></a> | ./wms:Capability/wms:Layer/BoundingBox
@CRS <a name="CRS"></a> | ./wms:Capability/wms:Layer/BoundingBox[@CRS]
